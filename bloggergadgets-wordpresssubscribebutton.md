# Instructions
1. Set up a WordPress blog
2. Find your siteID in your WordPress blog’s View Source code. In the template provided below in the next section, copy the template to a notepad (or Apple Notes) and replace my siteID with your own from your WordPress blog
3. The postID in your WordPress blog’s View Source code is set as 0 for the homepage, keep it as this
4. In the template below, copy the template to a notepad (or Apple Notes) and replace my nonce with your own from your WordPress blog
5. In the template below, change my Blogger url for your own
6. Where it says RSD in the template, change this for your own on your WordPress blog
7. Where it says actnbr-reader in the template, change the number value to the one included in your WordPress blog’s View Source code
8. Visit blogger.com, login and then select your blog
9. On your admin dashboard for your blog, head to the dropdown menu in the top left of the screen and right-click the link to Theme and open it in another tab
10. Head to Customize and type the following **BEFORE** the end head tag in your Blogger’s template theme. I’ve included the end head tag below for your convenience

# Blogger Template
```
<script id="wpcom-actionbar-placeholder-js-extra">
var actionbardata = {"siteID":"95140160","postID":"0","siteURL":"https:\/\/warrenwoodhouse.blogspot.com","xhrURL":"https:\/\/warrenwoodhouse.wordpress.com\/wp-admin\/admin-ajax.php","nonce":"512af0c249","isLoggedIn":"","statusMessage":"","subsEmailDefault":"instantly","proxyScriptUrl":"https:\/\/s0.wp.com\/wp-content\/js\/wpcom-proxy-request.js?ver=20211021","shortlink":"https:\/\/warrenwoodhouse.blogspot.com","i18n":
{"followedText":"New posts from this blog will now appear in your <a href=\"https:\/\/[wordpress.com](http://wordpress.com/)\/reader\">WordPress Reader<\/a>","foldBar":"Collapse this bar","unfoldBar":"Expand this bar","shortlinkCopied":"Blog link copied to clipboard."}};
</script>
<link rel="EditURI"  
type="application/rsd+xml"  
title="RSD" href="https://warrenwoodhouse.wordpress.com/xmlrpc.php?rsd" />
</head>
```

# Footer
This code goes in the footer section of your Blogger blog. Open up the dashboard for your blog on Blogger, navigate to Layout and in the footer section, select add gadget then select HTML/JavaScript. The following code must be placed in there however like earlier, change the values and information to match your WordPress blog and Blogger blog.

This code goes in the Footer. Like before, change the values and data to match your WordPress blog's siteID, postID and RSD for the code to work correctly.
```
<div id="actionbar" dir="ltr" style="display: none;"
			class="actnbr-pub-minileven actnbr-has-follow actnbr-has-actions">
		<ul>
								<li class="actnbr-btn actnbr-hidden">
								<a class="actnbr-action actnbr-actn-follow " href="">
			<svg class="gridicon" height="20" width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path clip-rule="evenodd" d="m4 4.5h12v6.5h1.5v-6.5-1.5h-1.5-12-1.5v1.5 10.5c0 1.1046.89543 2 2 2h7v-1.5h-7c-.27614 0-.5-.2239-.5-.5zm10.5 2h-9v1.5h9zm-5 3h-4v1.5h4zm3.5 1.5h-1v1h1zm-1-1.5h-1.5v1.5 1 1.5h1.5 1 1.5v-1.5-1-1.5h-1.5zm-2.5 2.5h-4v1.5h4zm6.5 1.25h1.5v2.25h2.25v1.5h-2.25v2.25h-1.5v-2.25h-2.25v-1.5h2.25z"  fill-rule="evenodd"></path></svg>
			<span>Subscribe</span>
		</a>
		<a class="actnbr-action actnbr-actn-following  no-display" href="">
			<svg class="gridicon" height="20" width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path fill-rule="evenodd" clip-rule="evenodd" d="M16 4.5H4V15C4 15.2761 4.22386 15.5 4.5 15.5H11.5V17H4.5C3.39543 17 2.5 16.1046 2.5 15V4.5V3H4H16H17.5V4.5V12.5H16V4.5ZM5.5 6.5H14.5V8H5.5V6.5ZM5.5 9.5H9.5V11H5.5V9.5ZM12 11H13V12H12V11ZM10.5 9.5H12H13H14.5V11V12V13.5H13H12H10.5V12V11V9.5ZM5.5 12H9.5V13.5H5.5V12Z" fill="#008A20"></path><path class="following-icon-tick" d="M13.5 16L15.5 18L19 14.5" stroke="#008A20" stroke-width="1.5"></path></svg>
			<span>Subscribed</span>
		</a>
							<div class="actnbr-popover tip tip-top-left actnbr-notice" id="follow-bubble">
							<div class="tip-arrow"></div>
							<div class="tip-inner actnbr-follow-bubble">
															<ul>
											<li class="actnbr-sitename">
			<a href="https://warrenwoodhouse.blogspot.com/">
				<img loading='lazy' alt='' src='[https://warrenwoodhouse.blogspot.com/favicon.ico?w=50](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=50)' srcset='[https://warrenwoodhouse.blogspot.com/favicon.ico?w=49](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=49) 1x, [https://warrenwoodhouse.blogspot.com/favicon.ico?w=74](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=74) 1.5x, [https://warrenwoodhouse.blogspot.com/favicon.ico?w=78](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=78) 2x, [https://warrenwoodhouse.blogspot.com/favicon.ico?w=78](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=78) 3x, [https://warrenwoodhouse.blogspot.com/favicon.ico?w=78](https://warrenwoodhouse.wordpress.com/wp-content/uploads/2014/07/emblem-warrenwoodhouse.png?w=78) 4x' class='avatar avatar-50' height='50' width='50' />				Warren Woodhouse			</a>
		</li>
										<div class="actnbr-message no-display"></div>
									<form method="post" action="https://subscribe.wordpress.com/" accept-charset="utf-8" style="display: none;">
																				<div>
										<input type="email" name="email" placeholder="Enter your email address" class="actnbr-email-field" aria-label="Enter your email address" />
										</div>
										<input type="hidden" name="action" value="subscribe" />
										<input type="hidden" name="blog_id" value="95140160" />
										<input type="hidden" name="source" value="https://warrenwoodhouse.blogspot.com/" />
										<input type="hidden" name="sub-type" value="actionbar-follow" />
										<input type="hidden" id="_wpnonce" name="_wpnonce" value="9556989cd5" />										<div class="actnbr-button-wrap">
											<button type="submit" value="Sign me up">
												Sign me up											</button>
										</div>
									</form>
									<li class="actnbr-login-nudge">
										<div>
											Already have a Blogger account? <a href="https://warrenwoodhouse.blogspot.com/login">Log in now.</a>										</div>
									</li>
								</ul>
															</div>
						</div>
					</li>
									<li class="actnbr-btn actnbr-hidden no-display" onclick="javascript:__tcfapi( 'showUi' );">
						<a class="actnbr-action actnbr-actn-privacy" href="#">
							<svg class="gridicon gridicons-info-outline" height="20" width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g><path d="M13 9h-2V7h2v2zm0 2h-2v6h2v-6zm-1-7c-4.41 0-8 3.59-8 8s3.59 8 8 8 8-3.59 8-8-3.59-8-8-8m0-2c5.523 0 10 4.477 10 10s-4.477 10-10 10S2 17.523 2 12 6.477 2 12 2z"/></g></svg>							<span>Privacy						</span>
						</a>
					</li>
							<li class="actnbr-ellipsis actnbr-hidden">
				<svg class="gridicon gridicons-ellipsis" height="24" width="24" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g><path d="M7 12c0 1.104-.896 2-2 2s-2-.896-2-2 .896-2 2-2 2 .896 2 2zm12-2c-1.104 0-2 .896-2 2s.896 2 2 2 2-.896 2-2-.896-2-2-2zm-7 0c-1.104 0-2 .896-2 2s.896 2 2 2 2-.896 2-2-.896-2-2-2z"/></g></svg>				<div class="actnbr-popover tip tip-top-left actnbr-more">
					<div class="tip-arrow"></div>
					<div class="tip-inner">
						<ul>
								<li class="actnbr-sitename">
			<a href="https://warrenwoodhouse.blogspot.com">
				<img loading='lazy' alt='' src='https://warrenwoodhouse.blogspot.com/favicon.ico?w=50' srcset='https://warrenwoodhouse.blogspot.com/favicon.ico?w=49 1x, https://warrenwoodhouse.blogspot.com/favicon.ico?w=74 1.5x, https://warrenwoodhouse.blogspot.com/favicon.ico?w=78 2x, https://warrenwoodhouse.blogspot.com/favicon.ico?w=78 3x, https://warrenwoodhouse.blogspot.com/favicon.ico?w=78 4x' class='avatar avatar-50' height='50' width='50' />				Warren Woodhouse			</a>
		</li>
								<li class="actnbr-folded-follow">
										<a class="actnbr-action actnbr-actn-follow " href="">
			<svg class="gridicon" height="20" width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path clip-rule="evenodd" d="m4 4.5h12v6.5h1.5v-6.5-1.5h-1.5-12-1.5v1.5 10.5c0 1.1046.89543 2 2 2h7v-1.5h-7c-.27614 0-.5-.2239-.5-.5zm10.5 2h-9v1.5h9zm-5 3h-4v1.5h4zm3.5 1.5h-1v1h1zm-1-1.5h-1.5v1.5 1 1.5h1.5 1 1.5v-1.5-1-1.5h-1.5zm-2.5 2.5h-4v1.5h4zm6.5 1.25h1.5v2.25h2.25v1.5h-2.25v2.25h-1.5v-2.25h-2.25v-1.5h2.25z"  fill-rule="evenodd"></path></svg>
			<span>Subscribe</span>
		</a>
		<a class="actnbr-action actnbr-actn-following  no-display" href="">
			<svg class="gridicon" height="20" width="20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path fill-rule="evenodd" clip-rule="evenodd" d="M16 4.5H4V15C4 15.2761 4.22386 15.5 4.5 15.5H11.5V17H4.5C3.39543 17 2.5 16.1046 2.5 15V4.5V3H4H16H17.5V4.5V12.5H16V4.5ZM5.5 6.5H14.5V8H5.5V6.5ZM5.5 9.5H9.5V11H5.5V9.5ZM12 11H13V12H12V11ZM10.5 9.5H12H13H14.5V11V12V13.5H13H12H10.5V12V11V9.5ZM5.5 12H9.5V13.5H5.5V12Z" fill="#008A20"></path><path class="following-icon-tick" d="M13.5 16L15.5 18L19 14.5" stroke="#008A20" stroke-width="1.5"></path></svg>
			<span>Subscribed</span>
		</a>
								</li>
														<li class="actnbr-signup"><a href="https://warrenwoodhouse.blogspot.com/signup">Sign up</a></li>
							<li class="actnbr-login"><a href="https://warrenwoodhouse.blogspot.com/login">Log in</a></li>
															<li class="flb-report">
									<a href="https://wordpress.com/abuse/?report_url=https://warrenwoodhouse.blogspot.com" target="_blank" rel="noopener noreferrer">
										Report this content									</a>
								</li>
															<li class="actnbr-reader">
									<a href="https://wordpress.com/reader/feeds/95140160">
										View blog in Reader									</a>
								</li>
															<li class="actnbr-subs">
									<a href="https://subscribe.wordpress.com/">Manage subscriptions</a>
								</li>
																<li class="actnbr-fold"><a href="">Collapse this bar</a></li>
														</ul>
					</div>
				</div>
			</li>
		</ul>
	</div>
	
<script>
window.addEventListener( "DOMContentLoaded", function( event ) {
	var link = document.createElement( "link" );
	link.href = "https://warrenwoodhouse.wordpress.com/wp-content/mu-plugins/actionbar/actionbar.css?v=20250116";
	link.type = "text/css";
	link.rel = "stylesheet";
	document.head.appendChild( link );

	var script = document.createElement( "script" );
	script.src = "https://warrenwoodhouse.wordpress.com/wp-content/mu-plugins/actionbar/actionbar.js?v=20250204";
	document.body.appendChild( script );
} );
</script>
```
