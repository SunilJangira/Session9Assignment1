# Session9Assignment1

a. What is dialog?
Dialog is window (small) which coordinates with the end user with a message and with some buttons / options (YES/NO).
A dialog does not fill the screen and is normally used for modal events that require users to take an action before they can proceed.



b. How to create custom dialog?
The Dialog class is the base class for dialogs.
 subclasses:AlertDialog
A dialog that can show a title, up to three buttons, a list of selectable items, or a custom layout.
DatePickerDialog or TimePickerDialog

A dialog with a pre-defined UI that allows the user to select a date or time.
To build an AlertDialog:

 1. Instantiate an AlertDialog.Builder with its constructor
AlertDialog.Builder alertBuilder = new AlertDialog.Builder(getActivity());

2. Chain together various setter methods to set the dialog characteristics
alertBuilder.setMessage(R.string.dialog_message)
       .setTitle(R.string.dialog_title);

3. Get the AlertDialog from create()
AlertDialog dialog = alertBuilder.create();

If you want a custom layout in a dialog, 
create a layout and add it to an AlertDialog by calling setView() on your AlertDialog.Builder object.
 AlertDialog.Builder builder = new AlertDialog.Builder(getActivity());
    // Get the layout inflater
    LayoutInflater inflater = getActivity().getLayoutInflater();

    // Inflate and set the layout for the dialog
    // Pass null as the parent view because its going in the dialog layout
    builder.setView(inflater.inflate(R.layout.dialog_signin, null))
    
c. How to use existing dialogs?
DialogFragment can implement the onCreateDialog method and return an existing dialog. 
The Dialog class is the base class for implementing a dialog.
Typically, you use one of its subclasses, e.g., AlertDialog, ProgressDialog, DatePickerDialog or TimePickerDialog.

Android also provides a ProgressDialog, which can be opened via a ProgressDialog.open() method call.


