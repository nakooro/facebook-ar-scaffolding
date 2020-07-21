# facebook-ar-scaffolding

```sequence
Note left of User: Start
User->Me: User navigates to a product template
Me-->User: Me displays TryNow button
User->Me: User clicks on TryNow button

Me->Webview: Me generates the user's hash_psid 

Webview->Server: Webview  queries tracking userids \n 
Server-->Webview: Server returns tracking userids

Webview->Server: Webview queries AR's status 
Webview->Server: Webview sends the hash_psid




Server-->User:  Webview shows Fb's installation page (timeout)
Note left of User: End


Webview->AR:Webview opens AR via (deeplink)
Webview->AR: Webview sends arguments via (camerasharearguments)
AR-->User: AR opens in Fb
AR->Server: update AR's status

User->Me: User switches back to Me
Me->Webview: 

Server-->Webview: Server returns AR's status
Webview-->User: User receives the page according  to the AR's status

Note left of User: End



