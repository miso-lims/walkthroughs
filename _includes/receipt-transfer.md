When receiving {{ include.type_plural }}, you can enter some receipt information including a date and time, the lab that
the {{ include.type_plural }} came from, the internal group who was responsible for receiving them, a verification that
they were received as expected, and that a QC check was performed on them. Entering this information causes a _Transfer_
to be recorded. We will have a look at the transfer that was created from the data you entered in exercise
{{ include.items_exercise }}.

1. On the main menu under _Preparation_, click _{{ include.type_plural | capitalize }}_.
1. Click the alias of a {{ include.type }} you created in exercise {{ include.items_exercise }}. This takes you to the
   Edit {{ include.type | capitalize }} page, which gives you a detailed view of the individual {{ include.type }} and
   other items related to it.
1. On the Edit {{ include.type | capitalize }} page, scroll down to the _Transfers_ section. You should see a single
   transfer in the list.
1. Click the ID of the transfer to go to the Edit Transfer page, which gives you a more detailed view of the transfer.
1. Scroll down and look at the _Items_ section on the Edit Transfer page. If you create multiple items in the same
   project with the same date and time of receipt, they will be included in the same transfer.

Receipts are one type of transfer. You can also create internal transfers when items are transferred between different
groups within your organization, and distribution transfers when items are transferred out of the organization. This
allows you to track the complete chain of custody.
