================
Permissions list
================

Permission is an entity which grants access to certain functionality. Here you can find list of all permissions on the platform. There are 2 types of permisisons: account permissions and mailbox permissions. 

* Account permissions cover admin panel functionality.
* Mailbox permissions cover main application functionality.

.. _accountPermissions:

Account permissions
===================

.. list-table::
   :widths: 20 10 70
   :header-rows: 1

   * - Name
     - Code
     - Description
   * - userAssignToAccount
     - 10000
     - Allows to add permissions or roles to account
   * - userUnassignFromAccount
     - 10001
     - Allows to remove permissions from the account and remove user from account with special functionality
   * - rolesManage
     - 10002
     - Allows to create, clone and edit roles in particular account
   * - rolesDelete
     - 10003
     - Allows to remove roles in particular account
   * - mailboxManage
     - 10004
     - Allows to create and edit mailboxes in particular account
   * - mailboxArchive
     - 10005
     - Allows to archive mailboxes in particular account
   * - mailboxDelete
     - 10006
     - Allows to remove mailboxes in particular account
   * - accountManage
     - 10007
     - Allows to manage account settings of the particular account
   * - accountDelete
     - 10008
     - Allows to remove particular account (for which applied permissions)
   * - aliasCreate
     - 10009
     - Allows to create and edit mailbox aliases in particular account
   * - aliasDelete
     - 10010
     - Allows to remove mailbox aliases in particular account
   * - userAssignToMailbox
     - 10011
     - Allows to permissions or roles to mailboxes
   * - userUnassignFromMailbox
     - 10012
     - Allows to remove permissions from the mailboxes and remove user from mailboxes with special functionality
   * - userListView
     - 10013
     - Allows to view users list page
   * - rolesListView
     - 10014
     - Allows to view roles list page
   * - mailboxListView
     - 10015
     - Allows to view mailboxes list page
   * - auditLogView
     - 10016
     - Allows to view audit log page
   * - dashboardManage
     - 10017
     - Allows to configure custom dashboard page
   * - mailboxGroupView
     - 10018
     - Allows to view mailbox group list page
   * - mailboxGroupManage
     - 10019
     - Allows to create and edit mailbox groups
   * - mailboxGroupAssign 
     - 10020
     - Allows to add mailboxes to a group
   * - integrationView 
     - 10021
     - Allows to view integration list page
   * - integrationManage 
     - 10022
     - Allows to create, edit and remove conversion rules
   * - domainListView
     - 10100
     - Allows to view domains list page
   * - domainManage
     - 10101
     - Allows to add and edit domains configuration in particular account
   * - corporateUserManage
     - 10120
     - Allows to manage corporate users which belong to particular account
   * - accountView
     - 10130
     - Allows to view account settings page
   * - externalLinkListView
     - 10200
     - Allows to view external links page
   * - externalLinkManage
     - 10201
     - Allows to add abd edit external links
   * - externalLinkDelete
     - 10202
     - Allows to remove external links
   * - billingTariffView
     - 10211
     - Allows to view billing plans page
   * - billingTariffManage 
     - 10212
     - Allows to change plan on the billing page
   * - billingInvoiceView 
     - 10213
     - Allows to view invoices list page
   * - billingInvoicePayment 
     - 10214
     - Allows to pay invoices

.. _mailboxPermissions:

Mailbox permissions
===================

.. list-table::
   :widths: 20 10 70
   :header-rows: 1

   * - Name
     - Code
     - Description
   * - templateManage
     - 1000
     - Allows to create, clone and edit tempaltes in particular mailbox
   * - templateArchive
     - 1001
     - Allows to remove tempaltes in particular mailbox
   * - templateListView
     - 1002
     - Allows to view templates list and elements on dashboard which related to template list (block with recently used templates)
   * - envelopeManage
     - 2000
     - Allows to create and update drafts of the envelopes in particular mailbox
   * - envelopeSend
     - 2001
     - Allows to send envelope drafts in particular mailbox
   * - envelopeArchive
     - 2002
     - Allows to archive and unarchive envelopes in particular mailbox
   * - envelopeSign
     - 2003
     - Allows to fill envelope fields including digital signatures in envelope processing flow in particular mailbox
   * - envelopeListView
     - 2004
     - Allows to view envelopes list and elements on dashboard which related to envelope list (counters and wwaiting for you block)
   * - envelopeCommentRead 
     - 2005
     - Allows to view comments added to an envelope
   * - envelopeCommentWrite 
     - 2006
     - Allows to create, edit, solve, resolve and remove envelope comments
   * - envelopeChainAdd  
     - 2007
     - Allows to chain envelope with another envelope or envelopes
   * - envelopeChainRemove  
     - 2008
     - Allows to remove envelope from chain
   * - approvalFlowManage  
     - 2009
     - Allows to view, create, edit and remove approval routes
   * - envelopeApproval   
     - 2010
     - Allows to send envelopes to approval
   * - envelopeApprove
     - 2011
     - Allows to approve or decline envelopes on approval
   * - envelopeDelegate
     - 2012
     - Allows to delegate envelopes and configure automatic forwarding rule for mailbox
   * - approvalFlowShare
     - 2013
     - Allows to share envelopes approval routes
   * - envelopeCallbackManage
     - 2014
     - Allows to create, edit and remove callbacks
   * - envelopeRecycleBin
     - 2015
     - Allows to delete envelopes
   * - envelopeAuditTrailRecord 
     - 2016
     - Allows to add record to audit trail via API
   * - envelopeDownloadBinaries
     - 2017
     - Allows to download and print envelope documents
   * - envelopeShare
     - 2018
     - Allows to share envelopes by email or share access to envelope
   * - envelopeApprovalListView
     - 2019
     - Allows to view envelopes on approval list page
   * - categoryManage
     - 3000
     - Allows to create, update and move categories in particular mailbox
   * - categoryDelete
     - 3001
     - Allows to remove categories in particular mailbox
   * - dictionaryManage
     - 5000
     - Allows to create, update dictionaries and add, update columns in dictionaries in particular mailbox
   * - dictionaryArchive
     - 5001
     - Allows to remove dictionaries and remove columns inside dictionary in particular mailbox
   * - dictionaryRowManage
     - 5002
     - Allows to add and update rows inside dictionaries in particular mailbox
   * - dictionaryRowDelete
     - 5003
     - Allows to remove rows inside dictionaries in particular mailbox
   * - dictionaryListView
     - 5004
     - Allows to view dictionaries list page
   * - labelManage
     - 6000
     - Allows to create and update labels in particular mailbox
   * - labelDelete
     - 6001
     - Allows to remove labels in particular mailbox
   * - labelAssignManage
     - 6002
     - Allows to assign and unassign labels from envelopes in particular mailbox
   * - contactManage
     - 8000
     - Allows to create and update contacts in particular mailbox
   * - contactDelete
     - 8001
     - Allows to remove contacts in particular mailbox
   * - contactListView
     - 8002
     - Allows to view contacts list page
   * - integrationView
     - 9000
     - Allows to view integrations page
   * - integrationManage
     - 9001
     - Allows to configure integration and create, update and delete integration rules for particular mailbox
   * - scenarioList
     - 10000
     - Allows to view scenarios list page
   * - scenarioManage
     - 10001
     - Allows to create, update, clone scenarios in particular mailbox
   * - scenarioDelete
     - 10002
     - Allows to remove scenarios in particular mailbox