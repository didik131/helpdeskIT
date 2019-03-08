# Configure OpenSupports settings

## Email Settings
`Email server address`: Indicates the email address that will be on the `from` and `replyTo` parts of the email.
`Image header URL`: Indicates the url of the header image to be shown in the sent emails. By default it's OpenSupports' logo

### Configure SMTP
1. Configure `Email server address`
2. `SMTP Server`: Indicate the server with it's port in this format `{HOST}:{PORT}`, for example `tls://smtp.gmail.com:586`
3. `SMTP User`/`SMTP Password`: Indicate the SMTP credentials.
4. Make sure to hit `TEST` button to check the connection is working
5. Click `Save` when you're ready

### Configure IMAP
For creating tickets from emails, we connect to an IMAP server folder, check the messages, create tickets based on those and the delete the emails.

1. Configure `Email server address`. Do not use a `noreply` address.
2. `IMAP Server`: Indicate host with with folder to check emails, for example `{imap.gmail.com:993/imap/ssl}INBOX`
3. `IMAP User`/`IMAP Password`: Indicate the IMAP credentials.
4. Generate a `IMAP Token`. This serves as password for polling the emails.
5. Make sure to hit `TEST` button to check the connection is working.
6. Click `Save` when you're ready.

Remember to take a look to the infobox below. To parse emails and create tickets, you have to make a POST request to the indicated url and provide the `IMAP Token`. It's recommended to make it frequently, for example you can use a hook that calls it every time an email is received.
