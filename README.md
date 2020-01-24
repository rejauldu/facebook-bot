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
</ol>
<p>Now, go to your facebook inbox and send message to this new page. You send either 'Hi' or 'Hello'</p>
<p><strong>Source:</strong> <a href="https://tutorials.botsfloor.com/building-a-facebook-messenger-trivia-bot-with-laravel-part-1-61209b0e35db">Click</a></p>
<h1>Related tutorial</h1>
<h2>And here are the simple steps to getting your messenger chatbot on your site:</h2>
<ol>
<li>Go to your business Facebook page</li>
<li>Select Settings from the menu bar</li>
<li>From the left column, select Messenger Platform</li>
<li>Scroll to the Customer Chat Plugin section and hit “Set up”</li>
<li>Follow the Facebook prompts to:
<ul>
<li>Customize your greeting</li>
<li>Set your response time (give this some thought so you are setting the right expectation with your viewer.)</li>
<li>Choose your custom colors to stay true to your brand</li>
<li>Grab the html code to install yourself or select “email instructions to your developers” to send it right over to your website manager</li>
</ul>
</li>
</ol>