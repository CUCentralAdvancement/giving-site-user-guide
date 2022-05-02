# Gift Processor User Role

Gift Processors (GP) control all the aspects of how donations are processed on the website including editing Order 
statuses and downloading Order Processing Reports.

## Daily Tasks

The Gift Processor has three daily tasks they need to complete:

- [Credit Card Processing Report](#credit-card-processing-report) - Any gifts made via credit cards
- [eCheck Processing Report](#echeck-processing-report) - Any gifts made via eCheck
- [Recurring Transactions Processing](#recurring-orders-processing) - Gifts that recurr on a schedule.

### Credit Card Processing Report

The credit card processing report shows all the non-recurring transactions that have been made on the website. Even 
though an order can have multiple transactions associated with it, this report excludes recurring transactions, and 
it only contains single transactions, one per order, of one-time donations.

1. Go to https://giving.cu.edu/admin/staff-dashboard/reports/creditcard-processing-report.
2. Set "Order/Payment Status" to "Completed Success".
3. ...possibly set the date range...
4. Click "Apply" to perform the search.
5. Scroll to the bottom of the page and click the "XLS" button to export the report as a CSV.
6. ...do some other stuff...

### eCheck Processing Report

eCheck orders are processed differently than credit card orders since they have a different way of being verified 
that takes much longer than a credit card order.

1. Go to https://giving.cu.edu/admin/staff-dashboard/reports/echeck-processing-report
2. ...I don't really know what happens here...

There is a detailed eCheck process report from June 2020: [eCheck Processes](echeck-process-06-2020.pdf)

Notes on process report...from the perspective of a developer for now...will refine later to make sense for a gift 
processor.

1. You can actually check on the eCheck transaction status. eCheck orders are treated the same as credit card orders 
   but simply have bank account information in place of credit card information.
   1. Ping API for details: https://developer.authorize.net/api/reference/index.html#transaction-reporting-get-transaction-details
   2. No way via webhooks though..
2. You can get a list of transactions, filter out all the eCheck orders, and then do something with that.
3. We can write code that warns of approaching the $100,000/month donation limit vs. manually checking.
4. It looks like after 07/21/2021 the eCheck orders stopped being set to "Completed" and are left in a "Pending" state.
5. Using a `variable_set()` for keeping track of which eCheck orders have been already set to pending via 
   `commerce_authnet_accept_cron()` could end up becoming bigger than the available space so a better method should 
   be developed...probably keep orders as completed if 99.9% of the time the eCheck orders go through.

### Recurring Orders Processing

To keep the recurring order transactions out of the main credit card processing report, a GP user needs to mark any 
recurring order as an ARB subscription after they enter the data in Authorize.net

Steps:
1. Go to https://giving.cu.edu/admin/commerce/recurring-orders and copy an order ID from the list.
2. Go to https://account.authorize.net/UI/themes/wellsfargo/merch.aspx?page=search&sub=batchlist and search for the 
   order ID under "Invoice #".
3. Click into the transaction via the "Trans ID" link.
4. Click on "Create ARB Subscription from Transaction" once on the Transaction Detail screen. 
5. Set the Subscription Interval to what the order says on the Giving website: Annually, Monthly, or Quarterly
6. ...not sure if you need to do anything with the date...
7. Save the new subscription in Authorize.net
8. Go back to the "New Recurring Requests" report, select the order row, and click "Mark as ARB Subscription" to 
   keep this order and transactions out of the credit card processing report.

