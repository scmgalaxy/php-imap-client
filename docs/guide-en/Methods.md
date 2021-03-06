# Methods

The following methods are currently available.

* ``__construct($mailbox, $username, $password, $encryption)`` open new imap connection
* ``isConnected()`` check whether the imap connection could be opened successfully
* ``getError()`` returns the last error message
* ``selectFolder($folder)`` select current folder
* ``getFolders($seperator, $type)`` @param string $separator. Default is '.' @param int $type. Has three meanings 0,1,2.If 0 return nested array, if 1 return an array of strings, if 2 return raw imap_list()
* ``setEmbed($val)`` If true, embed all 'inline' images into body HTML, accesible in 'body_embed'
* ``countMessages()`` count messages in current folder
* ``countUnreadMessages()`` count unread messages in current folder
* ``getMessages($withbody = true, $standard = "UNSEEN")`` get emails in current folder
* ``getMessage($id)`` get email by given id
* ``getUnreadMessages($withbody = true)`` get unread messages in current folder
* ``deleteMessage($id)`` delete message with given id
* ``deleteMessages($ids)`` delete messages with given ids (as array)
* ``moveMessage($id, $target)`` move message with given id in new folder
* ``moveMessages($ids, $target)`` move messages with given ids (as array) in new folder
* ``setUnseenMessage($id, $seen = true)`` set unseen state of the message with given id
* ``getAttachment($id, $index = 0)`` get attachment of the message with given id (getMessages returns all available attachments)
* ``getQuota($user)`` Retrieve the quota level settings, and usage statics per mailbox.
* ``getQuotaRoot($user)`` Retrieve the quota level settings, and usage statics per mailbox.
* ``addFolder($name)`` add new folder with given name
* ``removeFolder($name)`` delete folder with fiven name
* ``renameFolder($name, $newname)`` rename folder with given name
* ``purge()`` move all emails in the current folder into trash. emails in trash and spam will be deleted
* ``setEncoding()`` Identify encoding by charset attribute in header
* ``convertToUtf8()`` Apply encoding defined in header
* ``getAllEmailAddresses()`` returns all email addresses of all emails (for auto suggestion list)
* ``saveMessageInSent($header, $body)`` save a sent message in sent folder
* ``getMailboxStatistics()`` returns statistics, see [imap_mailboxmsginfo](http://php.net/manual/de/function.imap-mailboxmsginfo.php)
* ``saveEmail($file , $id, $part)`` saves an email to the $file file
* ``saveEmailSafe($file , $id, $part, $streamFilter)`` saves an email to the $file file. This is recommended for servers with low amounts of RAM. Stream filter is set to convert.base64-decode by default
* ``saveAttachmetsMessagesBySubject($subject, $dir = null, $charset = null)`` Save Attachmets Messages By Subject
* ``getBriefInfoMessages()`` Get a short information about the messages in the current folder.
* ``sendMail()`` Send a message via the adapter.
* ``getHeaderInfo($msgnumber)`` Get the header info via the message number. http://php.net/manual/en/function.imap-headerinfo.php#refsect1-function.imap-headerinfo-returnvalues
