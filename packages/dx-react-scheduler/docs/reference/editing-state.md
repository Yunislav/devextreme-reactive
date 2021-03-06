# EditingState Plugin Reference

A plugin that manages the scheduler appointment editing state.

## Import

Use the following statement to import the plugin:

```js
import { EditingState } from '@devexpress/dx-react-scheduler';
```

## User Reference

### Dependencies

none

### Properties

Name | Type | Default | Description
-----|------|---------|------------
editingAppointmentId? | number &#124; string | | The identifier of an appointment being edited.
defaultEditingAppointmentId? | number &#124; string | | The initial value of the `editingAppointmentId` property in uncontrolled mode.
onEditingAppointmentIdChange? | (editingAppointmentId: number &#124; string) => void | | Handles changes to the `editingAppointmentId` property value.
addedAppointment? | object | | A created but not committed appointment.
defaultAddedAppointment? | object | | The initial value of the `addedAppointment` property in uncontrolled mode.
onAddedAppointmentChange? | (addedAppointment: object) => void | | Handles changes to the `addedAppointment` property value.
appointmentChanges? | { [key: string]: object } | | Uncommitted appointment changes.
defaultAppointmentChanges? | { [key: string]: object } | | The initial value of the `appointmentChanges` property in uncontrolled mode.
onAppointmentChangesChange? | (appointmentChanges: { [key: string]: any }) => void | | Handles changes to the `appointmentChanges` property value.
onCommitChanges | (changes: [ChangeSet](#changeset)) => void | | Handles commiting appointment changes.

## Interfaces

### ChangeSet

Describes uncommitted changes made to the scheduler data.

Field | Type | Description
------|------|------------
added? | [AppointmentModel](./scheduler.md#appointmentmodel) | An appointment to be created.
changed? | { [key: number &#124; string]: object } | Changes made to an appointment. The item's key specifies the associated appointment's ID.
deleted? | number &#124; string | The identifier of an appointment to be deleted.
