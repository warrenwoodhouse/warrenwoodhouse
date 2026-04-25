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

[CLICK HERE](https://github.com/warrenwoodhouse/warrenwoodhouse/blob/master/bloggergadgets-footer-wordpressactionbar.md) to see the template in MARKDOWN format
