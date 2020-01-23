<h1>Instructions</h1>
<ol>
<li>Install laravel</li>
<li>Create two routes with the same names but different methods (ie. facebook-bot)</li>
<li>Crate BotController as like this project</li>
<li>Create BotMiddleware</li>
<li>Edit <code>app\Http\Kernel.php</code> >Add <code>'bot' => \App\Http\Middleware\BotMiddleware::class</code> in routeMiddleware</li>
<li>Edit <code>app\Http\Middleware\VerifyCsrfToken.php</code> > Add <code>'/facebook-bot'</code> into <code>$except[]</code></li>
<li>htdocs><code>npm install ngrok -g</code></li>
<li><code>ngrok authtoken 1Wnqn1PNPuWJj2iqxzl8sbEanKF_2hykXvSPPRQdkxrTtmXJg</code></li>
<li>Create virtual at <code>facebook-bot</code> folder</li>
<li><code>ngrok http -host-header=rewrite facebook-bot:80</code></li>
<li>Create New app (with messanger)</li>
<li>Create New page</li>
<li>Access Token>Add or Remove pages (add the created page above)</li>
<li>Generate token and copy to <code>FACEBOOK_PAGE_ACCESS_TOKEN</code></li>
<li>WebHooks>Add Callback URL<br/>
Callback URL><code>https://938b1d15.ngrok.io/facebook-bot</code> (url created by ngrok)<br/>
Verify Token><code>facebook_messanger_api</code> (value of FACEBOOK_MESSANGER_WEBHOOK_TOKEN of env)</li>
<li>Add Subscriptions> select subscription fields</li>
<p>Now, go to your inbox and send message to this new page. You send either 'Hi' or 'Hello'</p>