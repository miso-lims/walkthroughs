Several QC methods are supported in MISO. The same process can be used to add QCs to a single or multiple
{{ include.type_plural }} at once.

1. On the _{{ include.type_plural | capitalize }}_ list page, enter your project's
   {% if include.detailed == true %}short{% endif %} name in the search box and press the `Enter` key on your keyboard.
1. Check the boxes for the {{ include.type_plural }} that you created in exercise {{ include.items_section }}.
1. Click _Add QCs_ at the top left of the table.
1. Enter `1` QC per {{ include.type }} and `1` control per QC, and click _Add_.
1. Fill out the table for each row as follows:
    * _Date_: enter today's date
    * _Type_: Select one of the available QC methods.
    * _Instrument_: Depending on the QC type, you may have to indicate which instrument was used. If required, chose any
      instrument.
    * _Kit_: Depending on the QC type, you may have to indicate which kit was used. If required, choose any kit.
    * _Kit Lot_: If you entered a kit, also include a LOT#. Use the current date. e.g. `2020-07-17`
    * _Result_: Enter a value that makes sense for the QC. Some QCs are pass/fail, while others have a numerical result.
    * _Control 1_: Depending on the QC type, you may have to indicate which control(s) were used. If required, choose any
      control.
    * _Control 1 LOT#_: If you entered a control, also include a LOT# for it. Use the current date. e.g. `2020-07-17`.
    * _Control 1 Passed?_: If you entered a control, select `True` to indicate that the control ran as expected.
    * Click _Save_.

The QCs will now be visible on the individual Edit {{ include.type | capitalize }} page.

1. On the _{{ include.type_plural | capitalize }}_ list page, enter your project name in the search box and press the
   `Enter` key on your keyboard.
1. Click one of the {{ include.type_plural }} you previously selected.
1. Scroll down to the _QCs_ section. The QC you just entered should appear in the table.
