# CellPhone-To-Remailer

Send remailer messages via email to a mixmaster server.

MixMailFromUser.sh - Email from cell phone to Remailer

This script is run on a Linux server wherein mixmaster has
been installed.  The script will run with an installed
mixmaster client only.  It does not require a full mixmaster
remailer installation.

It was written for the purpose of sending remailer messages via
email from a cell phone.  Remailer headers and message must
be PGP symetrically encrypted using OpenKeyChain before it is
sent in order to mask the remailer message and headers.

Create a new user on your server.  That is all that needs
to be done concerning the new user.  Choose an inconspicuous
user name so as to not let on that it has anything to do
with a remailer.   This user will be the user that receives
the encrypted emails sent from your cell phone.

The program checks the 'var/mail/<username>' mail file for
text.  If text is found, it strips out all of the pgp bundles
and decrypts the mixmaster headers/message and sends the message
with the mixmaster client.  The script can handle multiple
received emails/pgp bundles if present.

This script is executred via cron every few minutes to process
incoming messages.

See futher setup instructions within the Script file.
