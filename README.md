<html>
 <head>
 	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
 </head>
  <body style="background-color: #fff;">
  <div class="twitter-block">
      <a class="twitter-timeline" data-width="300" data-height="601px" href="https://twitter.com/twitter" data-link-color="#000" data-theme="light" data-chrome="noheader transparent nofooter nofooter noborders">Tweets by</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
  </div>
      <script>
        $(window).on('load', function() {
    $('iframe[id^=twitter-widget-]').each(function () {
        var head = $(this).contents().find('head');
        if (head.length) {
            head.append('<style>::-webkit-scrollbar {width:.5em;height:.5em;}::-webkit-scrollbar-thumb {background:#666;}::-webkit-scrollbar-track {background:none;}.hht img.Avatar.Avatar--edge {border-radius: 4px !important;}.timeline-Widget { background-color: #eee !important;max-width: 100% !important; width: 100% !important;height:100% !important; } .timeline .stream { max-width: none !important; width: 100% !important; }.timeline-Tweet-retweetCredit { padding-bottom: 22px; }.timeline-Tweet-author.js-inViewportScribingTarget {border-bottom: 1px solid #cacccb;}p.timeline-Tweet-text {padding-top: 22px;}p.timeline-Tweet-text {padding-bottom: 22px;}ul.timeline-Tweet-actions {border-bottom: 1px solid #cacccb7a;}ul.timeline-Tweet-actions {padding-bottom: 8px;}ul.timeline-Tweet-actions {border-top: 1px solid #cacccb7a;}ul.timeline-Tweet-actions {padding-top: 8px;}.timeline-Tweet-author {border-bottom: 1px solid #cacccb7a;}a.PrettyLink.hashtag.customisable { color: #004892;text-shadow:0px 0px 0px #333;}.TweetAuthor.js-inViewportScribingTarget { padding-top:-11px;}.TweetAuthor.js-inViewportScribingTarget {padding-left: 21px;}.TweetAuthor-avatar {width: 100px;height: 100px;}.SandboxRoot.env-bp-min .timeline-Tweet-text {font-size: 13px;letter-spacing: 0.5px;color: #000;}span.TweetAuthor-name.Identity-name.customisable-highlight { text-transform: uppercase;}.TweetAuthor-name { font-size:16px; line-height: 23px;}a.PrettyLink.profile.customisable.h-card {color: #004892;}.timeline-Tweet-metadata {padding-top: 7px;padding-right: 30px;}.Icon.Icon--twitter {display: none;}span.TweetAuthor-screenName.Identity-screenName {display: none;}.timeline-Tweet-retweetCredit {display: none;}.SandboxRoot.env-bp-min .timeline-Tweet { padding: 15px;}.TweetAuthor.js-inViewportScribingTarget {padding-bottom: 0px;}span.Identity-name.TweetAuthor-name.customisable-highlight {padding-top: 12px;}.SandboxRoot.env-bp-min .timeline-Tweet-author {margin-top: -15px}.TweetAuthor.js-inViewportScribingTarget { padding-bottom: 0px;}span.Identity-name.TweetAuthor-name.customisable-highlight { padding-top: 31px;font-size: 14px;}.SandboxRoot.env-bp-min .timeline-Tweet-text {margin-top: 0px;}p.timeline-Tweet-text {padding-bottom: 15px;.SandboxRoot.env-bp-min .timeline-Tweet-author { margin-top: -34px;}.hht img.Avatar.Avatar--edge { border-radius: 10% !important;}</style>');
    }
        $('#twitter-widget-0').append($('<div class=timeline>'));
    })
});

         jQuery('.twitter-block').delegate('#twitter-widget-0','DOMSubtreeModified propertychange', function() {
  //function call to override the base twitter styles
  customizeTweetMedia();
 });
 
 var customizeTweetMedia = function() {
 
  //overrides font styles and removes the profile picture and media from twitter feed
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('.timeline-Tweet-media').css('display', 'block');
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('img.Avatar').css('display', 'block');
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('span.TweetAuthor-avatar.Identity-avatar').remove();
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('span.TweetAuthor-screenName').css('font-size', '13px');
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('span.TweetAuthor-screenName').css('font-family', 'Raleway');
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('.timeline-Viewport').addClass('hht');

 
 
  //also call the function on dynamic updates in addition to page load
  jQuery('.twitter-block').find('.twitter-timeline').contents().find('.timeline-TweetList').bind('DOMSubtreeModified propertychange', function() {
   customizeTweetMedia(this);
});
}
      </script>
     
  </body>
</html>
