# asterisk-ivr-directdial-return
Direct dial an extension from IVR and return to IVR if no answer.

We are assuming here that the extensions of the PBX are 2XX (from 200 to 299).

You should create a Custom Destination from FreePBX, with this target:
`ivr-directdialreturn,${EXTEN},1`

On the IVR where you want to achieve this functionality you should:
1. disable the direct dialing
2. create a destination with ext "\_2XX" and the custom destination mentioned above
