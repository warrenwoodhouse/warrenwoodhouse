```
<!-- Widget Name: Recent Comments Widget -->
<!-- Widget Author: Warren Woodhouse -->
<!-- Widget Documentation: https://warrenwoodhouse.blogspot.com/widgets/recentcomments -->

<div id="recent-comments-widget">Loading comments...</div>

<style>
  /* Style the widget container */
  #recent-comments-widget {
    font-family: Arial, sans-serif;
    font-size: 19px;
    line-height: 1.5;
  }
  /* Style each comment block */
  .rc-item {
    padding: 20px 0;
    border-bottom: 5px solid #000000;
    border-radius: 8px;
    background-color: #ffffff;
    margin-bottom: 10px;
  }
  .rc-item:last-child {
    border-bottom: none;
  }
  /* Style the author's name */
  .rc-author {
    font-weight: bold;
    color: #000000;
  }
  /* Style the text snippet */
  .rc-snippet {
    color: #000000;
  }
  /* Style the link back to the post */
  .rc-link {
    display: block;
    font-size: 16px;
    color: #000000;
    text-decoration: none;
    margin-top: 4px;
  }
  .rc-link:hover {
    text-decoration: underline;
  }
</style>

<script>
  function showRecentComments(json) {
    var numComments = 10; // Number of comments to show
    var container = document.getElementById('recent-comments-widget');
    var html = '';
    
    if (!json.feed.entry || json.feed.entry.length === 0) {
      container.innerHTML = 'No comments found.';
      return;
    }

    var entries = json.feed.entry;
    var count = Math.min(numComments, entries.length);

    for (var i = 0; i < count; i++) {
      var entry = entries[i];
      var authorName = entry.author[0].name.$t;
      
      // Get a clean snippet of the comment text
      var content = entry.summary ? entry.summary.$t : entry.content.$t;
      var cleanSnippet = content.replace(/<[^>]*>/g, '').substring(0, 100);
      if (content.length > 100) cleanSnippet += '...';

      // Find the link to the actual comment/post
      var commentUrl = '#';
      for (var j = 0; j < entry.link.length; j++) {
        if (entry.link[j].rel === 'alternate') {
          commentUrl = entry.link[j].href;
          break;
        }
      }

      // Construct the HTML for each item
      html += '<div class="rc-item">';
      html += '<span class="rc-author">' + authorName + '</span>: ';
      html += '<span class="rc-snippet">"' + cleanSnippet + '"</span>';
      html += '<a class="rc-link" href="' + commentUrl + '">View Comment →</a>';
      html += '</div>';
    }

    container.innerHTML = html;
  }
</script>

<!-- Fetch the comments feed from your own blog dynamically -->
<script src="/feeds/comments/default?alt=json-in-script&callback=showRecentComments&max-results=10"></script>
```
