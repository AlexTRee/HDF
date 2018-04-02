    
<!DOCTYPE html>
<html style="background-color: #F5F5F5">
<head>
				
		







	















		
	
			
	
	

					
		
		
			<title>Introduction to HDF5</title>
		<meta itemprop="name" content="Introduction to HDF5">			<meta name="twitter:title" content="Introduction to HDF5"> 		<meta property="og:title" content="Introduction to HDF5" /> 		
			<meta name="description" content="HDF5 Description" />
		<meta itemprop="description" content="HDF5 Description"> 		<meta name="twitter:description" content="HDF5 Description"> 		<meta property="og:description" content="HDF5 Description" /> 	
			<meta itemprop="image" content="https://confluence.hdfgroup.org/download/attachments/50078525/fileobj.png?version=1&amp;amp;modificationDate=1517514518882&amp;amp;api=v2"> 		<meta name="twitter:image:src" content="https://confluence.hdfgroup.org/download/attachments/50078525/fileobj.png?version=1&amp;amp;modificationDate=1517514518882&amp;amp;api=v2"> 		<meta property="og:image" content="https://confluence.hdfgroup.org/download/attachments/50078525/fileobj.png?version=1&amp;amp;modificationDate=1517514518882&amp;amp;api=v2" /> 	
	<meta property="og:url" content="https://confluence.hdfgroup.org/display/HDF5/Introduction+to+HDF5" /> 
				
		
	<meta property="og:site_name" content="Confluence" /> 
						
	
	    

	                    
    
	                    
    

		    
	    
	    
	    
	    

				    
	
		    
	
			<meta http-equiv="X-UA-Compatible" content="IE=EDGE,chrome=IE7">
<meta charset="UTF-8">
<meta id="confluence-context-path" name="confluence-context-path" content="">
<meta id="confluence-base-url" name="confluence-base-url" content="https://confluence.hdfgroup.org">

<meta id="atlassian-token" name="atlassian-token" content="3867c7a5dce2dd62d2502ed950115c70b0f66d13">


<meta id="confluence-space-key" name="confluence-space-key" content="HDF5">
<script type="text/javascript">
        var contextPath = '';
</script>

    

    <meta name="confluence-request-time" content="1522685092726">
        
            <script type="text/x-template" title="poll-selector-blueprint">
	<h3>What type of poll would you like to create?</h3>
	<div class="aui-group">
		<div class="aui-item">
			<div class="hero choice-poll">
				<h2>Choice poll</h2>
				<p>Use choice polls to make choices like where to go for lunch or to survey user satisfaction.</p>
				<p><a id="create-choice-poll" class="aui-button" href="#">Create choice poll</a></p>
			</div>
		</div>
		<div class="aui-item">
			<div class="hero date-poll">
				<h2>Date poll</h2>
				<p>Use date polls to schedule events like the next team meeting or an upcoming Atlassian User Group.</p>
				<p><a id="create-date-poll" class="aui-button" href="#">Create date poll</a></p>
			</div>
		</div>
	</div>
</script>

    
        
            <meta name="ajs-is-space-admin" content=""> <meta name="ajs-has-space-config" content="">
            <style>.ia-fixed-sidebar, .ia-splitter-left {width: 285px;}.theme-default .ia-splitter #main {margin-left: 285px;}.ia-fixed-sidebar {visibility: hidden;}</style>
            <meta name="ajs-use-keyboard-shortcuts" content="true">
            <meta name="ajs-discovered-plugin-features" content="$discoveredList">
            <meta name="stp-license-product-name" content="Confluence"/> <meta name="stp-license-days-to-expiry" content="452"/> <meta name="stp-license-is-admin" content="false"/> <meta name="stp-license-should-keep-banner-hidden" content="true"/>
            <meta name="ajs-keyboardshortcut-hash" content="81b40a79217a8a630da3de8f2d78edc7">
            <meta name="ajs-is-confluence-admin" content="false">
            <meta name="ajs-connection-timeout" content="10000">
            <meta name="gliffy-license-type" content="LicenseType&lt;COMMUNITY&gt;">
<meta name="gliffy-license-quantity" content="${pluginLicenseManager.userCount}">

            <script type="text/x-template" title="gliffy-webpanel-footer">
        <div class="gliffy-webpanel-footer"><span>This Confluence installation runs a Free Gliffy License - Evaluate the <a href="http://www.gliffy.com/products/confluence-plugin/">Gliffy Confluence Plugin</a> for your Wiki!</span></div>
</script>


            
    
    
            <meta name="ajs-page-id" content="50078525">
            <meta name="ajs-latest-page-id" content="50078525">
            <meta name="ajs-content-type" content="page">
            <meta name="ajs-page-title" content="Introduction to HDF5">
            <meta name="ajs-parent-page-title" content="Learning HDF5">
            <meta name="ajs-parent-page-id" content="48804307">
            <meta name="ajs-space-key" content="HDF5">
            <meta name="ajs-space-name" content="HDF5">
            <meta name="ajs-jira-metadata-count" content="0">
            <meta name="ajs-from-page-title" content="">
            <meta name="ajs-can-remove-page" content="false">
            <meta name="ajs-browse-page-tree-mode" content="view">
            <meta name="ajs-shared-drafts" content="false">
            <meta name="ajs-context-path" content="">
            <meta name="ajs-base-url" content="https://confluence.hdfgroup.org">
            <meta name="ajs-version-number" content="5.9.5">
            <meta name="ajs-build-number" content="6212">
            <meta name="ajs-remote-user" content="">
            <meta name="ajs-remote-user-key" content="">
            <meta name="ajs-remote-user-has-licensed-access" content="false">
            <meta name="ajs-current-user-fullname" content="">
            <meta name="ajs-current-user-avatar-url" content="">
            <meta name="ajs-static-resource-url-prefix" content="/s/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/_">
            <meta name="ajs-global-settings-attachment-max-size" content="102400000">
            <meta name="ajs-user-locale" content="en_GB">
            <meta name="ajs-enabled-dark-features" content="confluence.wrap.macro.disable,clc.quick.create,confluence.view.edit.transition,cql.search.screen,confluence-inline-comments-resolved,notification.plugin.api.enabled.com.atlassian.confluence.plugins.sharepage.api.ShareContentEvent,notification.plugin.api.enabled.com.atlassian.confluence.plugins.mentions.api.ConfluenceMentionEvent,nps.survey.inline.dialog,confluence.efi.onboarding.new.templates,notification.plugin.api.enabled.com.atlassian.confluence.event.events.security.ForgotPasswordEvent,pdf-preview,notification.plugin.api.enabled.com.atlassian.confluence.plugins.tasklist.event.SendTaskEmailEvent,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.page.async.PageMovedEvent,previews.sharing,previews.versions,notification.plugin.api.enabled.com.atlassian.confluence.plugins.files.notifications.event.FileContentUpdateEvent,file-annotations,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.attachment.AttachmentBatchUploadCompletedEvent,confluence.efi.onboarding.rich.space.content,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.comment.CommentCreateEvent,notification.plugin.api.enabled.com.atlassian.confluence.efi.emails.events.OnboardingLessUsersEvent,notification.plugin.api.enabled.com.atlassian.confluence.plugins.files.notifications.event.FileContentRemoveEvent,confluence.wrap.macro,atlassian.aui.raphael.disabled,previews.conversion-service,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.comment.CommentUpdateEvent,notification.plugin.api.enabled.com.atlassian.confluence.event.events.follow.FollowEvent,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.page.async.PageEditedEvent,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.blogpost.BlogPostCreateEvent,previews.trigger-all-file-types,notification.plugin.api.enabled.com.atlassian.confluence.plugins.inlinecomments.events.InlineCommentResolveEvent,notification.plugin.api.enabled.com.atlassian.confluence.event.events.like.LikeCreatedEvent,notification.plugin.api.enabled.com.atlassian.confluence.plugins.inlinecomments.events.InlineCommentCreateEvent,previews.sharing.pushstate,confluence-inline-comments-rich-editor,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.blogpost.BlogPostUpdateEvent,file-annotations.likes,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.page.async.PageCreatedEvent,notification.plugin.api.enabled.com.atlassian.confluence.plugins.files.notifications.event.FileContentMentionUpdateEvent,notification.plugin.api.enabled.com.atlassian.confluence.efi.emails.events.OnboardingNoSpaceCreatedEvent,notification.plugin.api.enabled.com.atlassian.confluence.plugins.hipchat.api.events.HipChatUserMapped,notification.plugin.api.enabled.com.atlassian.confluence.plugins.sharepage.api.ShareAttachmentEvent,confluence-inline-comments,quick-reload-inline-comments-flags,confluence-inline-comments-dangling-comment,notification.plugin.api.enabled.com.atlassian.confluence.event.events.content.blogpost.BlogPostMovedEvent">
            <meta name="ajs-atl-token" content="3867c7a5dce2dd62d2502ed950115c70b0f66d13">
            <meta name="ajs-confluence-flavour" content="VANILLA">
            <meta name="ajs-user-date-pattern" content="dd MMM yyyy">
            <meta name="ajs-date.format" content="MMM dd, yyyy">
    
    <link rel="shortcut icon" href="/s/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/_/favicon.ico">
    <link rel="icon" type="image/x-icon" href="/s/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/_/favicon.ico">

<link rel="search" type="application/opensearchdescription+xml" href="/opensearch/osd.action" title="Confluence"/>
    
                    
            <meta name="ajs-create-issue-metadata-show-discovery" content="false">
            

<script>
window.WRM=window.WRM||{};window.WRM._unparsedData=window.WRM._unparsedData||{};
WRM._unparsedData["com.atlassian.plugins.atlassian-plugins-webresource-plugin:context-path.context-path"]="\"\"";
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:atlassian-nps-plugin-resources.is-server-instance-data-provider"]="true";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:browser-metrics.feature-data-provider-legacy"]="true";
WRM._unparsedData["com.atlassian.plugins.atlassian-plugins-webresource-rest:web-resource-manager.resource-base-url-pattern"]="\"(?:(?:/s/.*?/_)?/download)\"";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-license-banner:confluence-license-banner-resources.license-details"]="{\"daysBeforeLicenseExpiry\":0,\"daysBeforeMaintenanceExpiry\":0,\"showLicenseExpiryBanner\":false,\"showMaintenanceExpiryBanner\":false,\"renewUrl\":null,\"salesEmail\":null}";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-hipchat-integration-plugin:discovery-javascript-data.link-active"]="{\"linkActive\":false,\"conditionsMet\":true,\"admin\":false}";
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:nps-acknowledgement-resources.analytics-enabled-data-provider"]="\"false\"";
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:nps-acknowledgement-resources.sen-data-provider"]="\"SEN-2026567\"";
WRM._unparsedData["com.onresolve.confluence.groovy.groovyrunner:web-item-response-renderer.web-item-actions-data-provider"]="[]";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-feature-discovery-plugin:confluence-feature-discovery-plugin-resources.test-mode"]="false";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:api.feature-data-provider"]="true";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:api.rack-data-provider"]="\"\"";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-context"]="{\"hostApplication\":{\"id\":\"0a60c7cc-4441-329b-a406-db7975d29eab\",\"type\":\"confluence\"}}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-features"]="{\"BITBUCKET_REBRAND\":true,\"V3_UI_OPT_IN\":false,\"V3_UI\":false}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-discovered-features"]="[]";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-context"]="{\"hostApplication\":{\"id\":\"0a60c7cc-4441-329b-a406-db7975d29eab\",\"type\":\"confluence\"}}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-features"]="{\"BITBUCKET_REBRAND\":true,\"V3_UI_OPT_IN\":false,\"V3_UI\":false}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-discovered-features"]="[]";
</script>
<link type="text/css" rel="stylesheet" href="/s/65c060fd7ba946af8fbeb7529927c19c-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/102/_/download/superbatch/css/batch.css" media="all">
<!--[if lt IE 9]>
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/102/_/download/superbatch/css/batch.css?conditionalComment=lt+IE+9" media="all">
<![endif]-->
<!--[if lte IE 9]>
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/102/_/download/superbatch/css/batch.css?conditionalComment=lte+IE+9" media="all">
<![endif]-->
<link type="text/css" rel="stylesheet" href="/s/49d531b57b6c1bc0901d5b42686ecf6b-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/44d282396c93e9460c059d9685706786/_/download/contextbatch/css/atl.confluence.plugins.pagetree-desktop,main,viewcontent,atl.general,page/batch.css?confluence.view.edit.transition=true&amp;highlightactions=true" media="all">
<!--[if lt IE 9]>
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/44d282396c93e9460c059d9685706786/_/download/contextbatch/css/atl.confluence.plugins.pagetree-desktop,main,viewcontent,atl.general,page/batch.css?conditionalComment=lt+IE+9" media="all">
<![endif]-->
<!--[if IE]>
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/44d282396c93e9460c059d9685706786/_/download/contextbatch/css/atl.confluence.plugins.pagetree-desktop,main,viewcontent,atl.general,page/batch.css?ieonly=true" media="all">
<![endif]-->
<link type="text/css" rel="stylesheet" href="/s/7e417bbc07ed21f90a55e989886f1017-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/5.7.34/_/download/batch/com.atlassian.auiplugin:aui-experimental-progress-tracker/com.atlassian.auiplugin:aui-experimental-progress-tracker.css" media="all">
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.2.13/_/download/batch/com.atlassian.confluence.plugins.confluence-previews:confluence-previews-css/com.atlassian.confluence.plugins.confluence-previews:confluence-previews-css.css" media="all">
<link type="text/css" rel="stylesheet" href="/s/d41d8cd98f00b204e9800998ecf8427e-T/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.6.12/_/download/batch/com.arsenale.plugins.lockpoint:lockpoint-fileviewer-resources/com.arsenale.plugins.lockpoint:lockpoint-fileviewer-resources.css" media="all">
<link type="text/css" rel="stylesheet" href="/s/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/3/_/styles/colors.css?spaceKey=HDF5" media="all">
<link type="text/css" rel="stylesheet" href="/s/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/2.1.1/_/download/resources/com.brikit.themepress:theme-base/default-theme.css" media="all">
<script type="text/javascript" src="/s/b5041722346a7574e2fdeb61b0309428-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/102/_/download/superbatch/js/batch.js?atlassian.aui.raphael.disabled=true&amp;locale=en-GB" ></script>
<script type="text/javascript" src="/s/f1678e0147d8c83a4847151083062d27-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/44d282396c93e9460c059d9685706786/_/download/contextbatch/js/atl.confluence.plugins.pagetree-desktop,main,viewcontent,atl.general,page/batch.js?confluence.view.edit.transition=true&amp;highlightactions=true&amp;nps-acknowledged=true&amp;locale=en-GB&amp;anonymous-access-enabled=true&amp;is-server-instance=true&amp;hostenabled=true" ></script>
<script type="text/javascript" src="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.0/_/download/batch/confluence.web.resources:moment/confluence.web.resources:moment.js" ></script>
<script type="text/javascript" src="/s/6c0981174e94142364564819dc0d1413-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.0/_/download/batch/confluence.web.resources:date-time-formatting/confluence.web.resources:date-time-formatting.js?locale=en-GB" ></script>
<script type="text/javascript" src="/s/6c0981174e94142364564819dc0d1413-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.2.13/_/download/batch/com.atlassian.confluence.plugins.confluence-previews:fileviewer-core/com.atlassian.confluence.plugins.confluence-previews:fileviewer-core.js?locale=en-GB" ></script>
<script type="text/javascript" src="/s/6c0981174e94142364564819dc0d1413-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.2.13/_/download/batch/com.atlassian.confluence.plugins.confluence-previews:confluence-previews-js/com.atlassian.confluence.plugins.confluence-previews:confluence-previews-js.js?locale=en-GB" ></script>
<script type="text/javascript" src="/s/6c0981174e94142364564819dc0d1413-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/3.4.16/_/download/batch/com.atlassian.confluence.extra.officeconnector:file-viewer-plugin/com.atlassian.confluence.extra.officeconnector:file-viewer-plugin.js?locale=en-GB" ></script>
<script type="text/javascript" src="/s/6c0981174e94142364564819dc0d1413-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.2.13/_/download/batch/com.atlassian.confluence.plugins.confluence-previews:upload-plugin/com.atlassian.confluence.plugins.confluence-previews:upload-plugin.js?locale=en-GB" ></script>
<script type="text/javascript" src="/s/d41d8cd98f00b204e9800998ecf8427e-CDN/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.6.12/_/download/batch/com.arsenale.plugins.lockpoint:lockpoint-versioncompare/com.arsenale.plugins.lockpoint:lockpoint-versioncompare.js" ></script>
<script type="text/javascript" src="/s/99914b932bd37a50b983c5e7c90ae93b-T/en_GB/6212/d125ddfe4e16e78d1fea8ef42a18979f09319385.57/1.6.12/_/download/batch/com.arsenale.plugins.lockpoint:lockpoint-fileviewer-resources/com.arsenale.plugins.lockpoint:lockpoint-fileviewer-resources.js?locale=en-GB" ></script>

    
        
            <meta name="stp-license-product-name" content="Confluence"/> <meta name="stp-license-days-to-expiry" content="452"/> <meta name="stp-license-is-admin" content="false"/> <meta name="stp-license-should-keep-banner-hidden" content="true"/>
    

        
        <meta name="ajs-site-title" content="Confluence" />

    

		<meta name="theme-press-version" content="2.1.1" />
	<meta name="theme-press-theme-name" content="Limelight" />
	<meta name="using-default-theme" content="false" />
	<meta name="brikit-developer-mode" content="false" />
	<meta name="ajs-allow-header" content="$themePress.headerAllowedFor($brikitThemeName)" />

				<meta name="ajs-show-header-by-default" content="nobody" />
			<meta name="anonymous-user" content="true" />
			<meta name="space-categories" content="support" />
	

	












		<meta name="ajs-full-page-url" content="/display/HDF5/Introduction+to+HDF5" />
	<meta name="ajs-page-url"      content="/display/HDF5/Introduction+to+HDF5" />

	<meta name="ancestor-link" value="/display/HDF5" />
		<meta name="ancestor-link" value="/display/HDF5/HDF5" />
		<meta name="ancestor-link" value="/display/HDF5/Learning+HDF5" />
	
	
		<link id="brikit-css-all" rel="stylesheet" type="text/css" href="/plugins/servlet/themepress/cssbundle/Limelight~~~411368135~~~all/combined.css" media="all" />
		<link id="brikit-css-print" rel="stylesheet" type="text/css" href="/plugins/servlet/themepress/cssbundle/Limelight~~~411368135~~~print/combined.css" media="print" />

		<script type="text/javascript" src="/plugins/servlet/themepress/jsbundle/Limelight~~~411368135~~~base~~~designer/combined.js"></script>
		<script type="text/javascript" src="/plugins/servlet/themepress/jsbundle/Limelight~~~411368135~~~theme~~~designer/combined.js"></script>


		
	
		<script type="text/javascript">
		themePressMobile = false; // window.screen.width < 640;
		themePressTablet = navigator.userAgent.toLowerCase().match(/(android|iphone|ipod|ipad|windows phone)/);
		var windowWidth = AJS.$(window).width();
		var screenWidth = window.screen.width;
		// Handle browser windows narrower than the content container
					var contentContainerWidth =  0;
				
		// Use content container + .brikit-toolbar padding-right for the container width
		if (themePressMobile) {			
			var viewportWidth = Math.min(windowWidth, screenWidth);
			document.write("<meta name='viewport' content='width=" + viewportWidth + ", initial-scale=1.0, user-scalable=no' />");
		}
		else if (themePressTablet) {
			var canvasWidth = contentContainerWidth > windowWidth ? contentContainerWidth + 24 : windowWidth;
			var scale = screenWidth / canvasWidth;
			document.write("<meta name='viewport' content='width=device-width, initial-scale=" + scale + ", user-scalable=yes' />");
		}
	
		AJS.$("meta[name='ajs-show-whats-new']").attr("content", "false");
	</script>

	

	
                <link rel="canonical" href="https://confluence.hdfgroup.org/display/HDF5/Introduction+to+HDF5">
        <link rel="shortlink" href="https://confluence.hdfgroup.org/x/PSP8Ag">
    <meta name="wikilink" content="[HDF5:Introduction to HDF5]">
    <meta name="page-version" content="57">


			<script>
		  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
		  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
		  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
		  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

		  ga('create', 'UA-3782034-5', 'auto');
		  ga('send', 'pageview');
		</script>
		
</head>




    

<body      id="com-atlassian-confluence" class="brikit theme-base   view-mode   page-context   aui-layout aui-theme-default   lighter-editor   confluence-header-hidden  space-category-support  ">


<div id="brikit-load-overlay" style="background-color: #F5F5F5; position:absolute; top:0px; left:0px; width:100%; height:100%; z-index:2000;"></div>


        
            <div id='stp-licenseStatus-banner'></div>
            <fieldset class="parameters hidden">
    <input type="hidden" id="workflowStatsUAKey" value="UA-11679828-12"/>
    
    
        </fieldset>
            
            <div id='workflow-page-status' style='display: none;'><fieldset class="hidden parameters">
<input type="hidden" id="hoverDescription" value="null"/><input type="hidden" id="finalState" value="false"/><input type="hidden" id="hasFinalState" value="false"/><input type="hidden" id="publishedView" value="false"/><input type="hidden" id="taskable" value="false"/><input type="hidden" id="activeTasks" value="0"/><input type="hidden" id="pageAssignable" value="false"/><input type="hidden" id="workflowAdmin" value="false"/><input type="hidden" id="anonymous" value="true"/><input type="hidden" id="activityVisible" value="false"/><input type="hidden" id="alternateViewTitle" value="View published version of page"/></fieldset></div>
<fieldset class="parameters hidden">
<input type="hidden" id="cwSpaceWorkflowAllowed" value="false"/>
<input type="hidden" id="tasksLabel" value="Tasks"/>
<input type="hidden" id="approvalsLabel" value="Approvals"/>
<input type="hidden" id="parametersLabel" value="Parameters"/>
<input type="hidden" id="statesLabel" value="State"/>
</fieldset><script type="text/x-template" title="adhocworkflows-loading">
    <div class="progress-messages-icon"></div>
</script>

<script type="text/x-template" title="adhocworkflows-user">
    <li class="preset"><img src="{pictureUrl}"><a name="{name}"><span>({name}) {shortName}</span></a></li>
</script>

<script type="text/x-template" title="adhocworkflows-assignee">
    <li class="assignee" name="{name}">
        <div>
            <img src="{pictureUrl}"/>{fullName}
            <span class="remove-assignee"></span>
        </div>
    </li>
</script>

<script type="text/x-template" title="adhoc-action">
    <span class="workflow-action {id}" name="{id}"></span>
</script>

<script type="text/x-template" title="adhocworkflows-approvals">
    <div class="progress-messages-icon"></div>
    <div id="workflow-main">
        <div class="approvals">
        </div>
        <form class="aui adhocworkflows">
            <div class="button-panel dialog">
                <a href="#" class="parameters">Parameters...</a>
                <a href="#" class="cancel-dialog">Cancel</a>
            </div>
        </form>
    </div>
</script>

<script type="text/x-template" title="adhocworkflows-approval-action-default">
    <span class="approval-name">{defaultAction.name}</span>
    <a name="{defaultAction.id}" class="approve workflow-action" href="#"><span>{defaultAction.shortName}</span></a>
</script>

<script type="text/x-template" title="adhocworkflows-approval-duedate">
    <div class="task-duedate">due {friendlyDueDate}</div>
</script>

<script type="text/x-template" title="adhocworkflows-approval">
    <div id="{id}" class="approval {separator}">
        <div class="approval-header clr">
            <div class="name {mark}">
            </div>
            <div class="approval-duedate">
            </div>
            <div class="workflow-actions">
            </div>
        </div>
        <div class="approval-edit">
            <div class="adhoc-message">
            </div>
            <form class="aui approval {signatureType}">
                <input type="hidden" name="name" value="{name}"/>
                <fieldset>
                    <div class="credential-username"><label for="username">User Name</label></div>
                    <input class="credential-username" type="text" name="username" id="username" width="10" >
                    <div class="credential-password"><label for="password">Password</label></div>
                    <input class="credential-password" type="password" name="password" id="password" width="10">
                                        <input  type="text"
                            class="text assignee-user"
                            name="assignee"
                            placeholder="Assign to..."/>
                                        <input  type="text"
                            class="text autocomplete-filtered-user"
                            users="{filterUsers}"
                            groups="{filterGroups}"
                            name="assignee"
                            data-max="10"
                            data-template="{username}"
                            data-none-message="No matching user found"
                            placeholder="Assign to..."/>
                    <div class="usersdropdown aui-dd-parent">
                        <a href="" class="aui-dd-trigger" style="display:none;"></a>
                        <div class="aui-dropdown aui-dropdown-left hidden">
                            <ol>
                            </ol>
                        </div>
                    </div>
                    <ol class="assignees select">
                    </ol>
                    <textarea class="textarea" placeholder="Add an optional note"/>
                </fieldset>
                <div class="button-panel">
                    <input type="submit" name="approve" class="approve" value="Approve">
                    <input type="submit" name="reject" class="reject" value="Reject">
                    <input type="submit" name="assign" class="assign" disabled="disabled" value="Assign">
                    <a href="#" class="cancel-approval">Cancel</a>
                </div>
            </form>

        </div>
    </div>
</script>

<script type="text/x-template" title="adhocworkflows-assignee-option">
    <option class="assigneename" value="{name}">
        <img src="{pictureUrl}" title="{fullName}"/>{fullName}
    </option>
</script>


<script type="text/x-template" title="adhocworkflows-approver">
    <div id="{id}" class="approval approver">
        <div class="approval-header clr">
            <div class="name {mark}">
                <img src="{user.pictureUrl}" title="{user.fullName}">
            </div>
            <div class="workflow-actions">
            </div>
        </div>
        <div class="approval-edit">
            <form class="aui approval {signatureType}">
                <input type="hidden" name="name" value="{name}"/>
                <fieldset>
                    <div class="credential-username"><label for="username">User Name</label></div>
                    <input class="credential-username" type="text" name="username" id="username" width="10" >
                    <div class="credential-password"><label for="password">Password</label></div>
                    <input class="credential-password" type="password" name="password" id="password" width="10">
                    <ol class="assignees assignee">
                    <li style="display:none" name="{user.name}"></li>
                    </ol>
                    <textarea class="textarea" placeholder="Add an optional note"/>
                </fieldset>
                <div class="button-panel">
                    <input type="submit" name="approve" class="approve" value="Approve">
                    <input type="submit" name="reject" class="reject" value="Reject">
                    <input type="submit" name="assign" class="assign" value="Assign">
                    <input type="submit" name="unassign" class="delete" value="Unassign">
                    <a href="#" class="cancel-approval">Cancel</a>
                </div>
            </form>

        </div>
    </div>
</script>

<script type="text/x-template" title="adhoctasks-tasks">
    <div class="progress-messages-icon"></div>
    <div id="tasks-main">
        <div class="tasks">
        </div>
        <form class="aui adhocworkflows addtask">
            <input type="hidden" name="id" value=""/>
            <fieldset>
                <span class="workflow-action assign-new-task" name="assign"></span>
                <input  id="taskName0"
                        name="taskName0"
                        class="text taskName active"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName1"
                        name="taskName1"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName2"
                        name="taskName2"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName3"
                        name="taskName3"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName4"
                        name="taskName4"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName5"
                        name="taskName5"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName6"
                        name="taskName6"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName7"
                        name="taskName7"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName8"
                        name="taskName8"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="taskName9"
                        name="taskName9"
                        class="text taskName"
                        type="text"
                        placeholder="Task name..."/>
                <input  id="newTaskAssignee"
                        type="text"
                        class="text autocomplete-user"
                        name="assignee"
                        data-max="10"
                        data-template="{username}"
                        data-none-message="No matching user found"
                        placeholder="Assign to..."/>
                <div class="usersdropdown aui-dd-parent">
                    <a href="" class="aui-dd-trigger" style="display:none;"></a>
                    <ul class="aui-dropdown aui-dropdown-left hidden">
                    </ul>
                </div>
                <ol class="assignees select single">
                </ol>
                <textarea class="textarea" placeholder="Add an optional note"/>
            </fieldset>
            <div class="button-panel">
                <a href="#" class="add-task">Add task...</a>
                <input type="submit" name="create" class="create" value="Create">
                <a href="#" class="cancel-addtask">Cancel</a>
                <a href="#" class="cancel-dialog">Cancel</a>
            </div>
        </form>
    </div>
</script>

<script type="text/x-template" title="adhoctasks-tasks-count">
    {count} Tasks
</script>

<script type="text/x-template" title="adhoctasks-tasks-count0">
    Tasks
</script>

<script type="text/x-template" title="adhoctasks-tasks-count1">
    1 Task
</script>

<script type="text/x-template" title="adhoctasks-task-action-default">
    <span class="task-name">{name}</span>
        <a name="{action.id}" class="workflow-action" title="{hint}" href="#">{shortName}</a>
</script>

<script type="text/x-template" title="adhoctasks-task-name">
    <span class="task-name">{name}</span>
</script>

<script type="text/x-template" title="adhoctasks-task-assignee">
    <img src="{user.pictureUrl}" title="{user.fullName}"> {user.fullName}
</script>

<script type="text/x-template" title="adhoctasks-task-duedate">
    <span class="task-duedate">due {friendlyDueDate}</span>
</script>

<script type="text/x-template" title="adhoctasks-task-completed">
    <div>
        {actor.fullName} {lastAction} {date}
    </div>
    <blockquote class="note">
        {comment}
    </blockquote>
</script>

<script type="text/x-template" title="adhoctasks-task">
    <div id="task-{id}" class="task {toggle}">
        <div class="task-header">
            <div class="name {completed}">
            </div>
            <div class="workflow-actions">
            </div>
        </div>
        <div class="task-edit">
            <div class="task-caption">
            </div>
            <form class="aui">
                <input type="hidden" name="id" value="{id}"/>
                <fieldset>
                    <input  type="text"
                            class="text autocomplete-user"
                            name="assignee"
                            data-max="10"
                            data-template="{username}"
                            data-none-message="No matching user found"
                            placeholder="Assign to..."/>
                    <div class="usersdropdown aui-dd-parent">
                        <a href="" class="aui-dd-trigger" style="display:none;"></a>
                        <ul class="aui-dropdown aui-dropdown-left hidden">
                        </ul>
                    </div>
                    <ol class="assignees select single">
                    </ol>
                    <textarea class="textarea" placeholder="Add an optional note"/>
                </fieldset>
                <div class="button-panel">
                    <input type="submit" name="remove" class="remove" value="Delete">
                    <input type="submit" name="complete" class="complete" value="Complete">
                    <input type="submit" name="assign" class="assign" value="Assign">
                    <a href="#" class="cancel-task">Cancel</a>
                </div>
            </form>
        </div>
    </div>
</script>
<script type="text/x-template" title="adhocworkflows-states">
    <div class="progress-messages-icon"></div>
    <div id="workflow-main">
        <form class="aui state">
            <fieldset>
                <span class="workflow-action assign-page" name="assign"></span>
                <select id="select-workflow-state" name="state">
                </select>
                <ol class="assignees assigned">
                </ol>
                <input type="text "
                            class="text newstatename"
                            placeholder="New State name"/>
                <input type="text"
                            class="text autocomplete-user"
                            name="assignee"
                            data-max="10"
                            data-template="{username}"
                            data-none-message="No matching user found"
                            placeholder="Assign to..."
                            placeholder2="Reassign to..."/>
                <div class="usersdropdown aui-dd-parent">
                    <a href="" class="aui-dd-trigger" style="display:none;"></a>
                    <ul class="aui-dropdown aui-dropdown-left hidden">
                    </ul>
                </div>
                <ol class="assignees select single">
                </ol>
                <textarea class="textarea" placeholder="Add an optional note"></textarea>
            </fieldset>
            <div class="button-panel">
                <input type="submit" name="change" class="accept" value="Accept">
                <input type="submit" name="unassign" class="unassign" value="Unassign">
                <a href="#" class="parameters">Parameters...</a>
                <a href="#" class="cancel-dialog">Cancel</a>
            </div>
        </form>
    </div>
</script>

<script type="text/x-template" title="adhocworkflows-state">
    <option>{name}</option>
</script>

<script type="text/x-template" title="adhocworkflows-state-adhoc">
    <optgroup label="Ad hoc Workflow">
        <option value="0">Create a new state...</option>
    </optgroup>
</script>

<script type="text/x-template" title="adhocworkflows-select">
    <div class="progress-messages-icon"></div>
    <form class="aui adhocworkflows">
        <fieldset>
            <label for="select-workflow-templates">Workflow</label>
            <select id="select-workflow-templates" name="workflowTemplate" class="select">
            </select>
            <div class="adhoc-states">
                <label for="adhoc-state-names">State names</label>
                <input id="adhoc-state-names" type="text" class="state-names" value="In Progress, Approved"/>
                <span class="description">
                    This is just an initial list, you will be able to change later
                </span>
            </div>

            <span class="description">
                Learn more about
                <a target="_blank" href="https://wiki.comalatech.com/x/lYDn">
                    working with workflows
                </a>
            </span>
        </fieldset>
        <div class="button-panel">
            <input type="submit" name="confirm" value="Add">
            <a href="#" class="close-dialog">Cancel</a>
        </div>

    </form>
</script>

<script type="text/x-template" title="adhocworkflows-adhoc-template">
    <optgroup label="Ad hoc Workflow">
        <option value="0" title="Use this to define the workflow as you go: at each step allow participants to create tasks and to decide where next to route the document. All the states and tasks will be recorded and you will be able to reuse the workflow.">Start with a blank workflow</option>
    </optgroup>
</script>

<script type="text/x-template" title="adhocworkflows-select-template">
    <option value="{id}" title="{description}">{name}</option>
</script>


<script type="text/x-template" title="adhocworkflows-form">
    <div class="progress-messages-icon"></div>
    <div id="workflow-form">
        <form class="aui ahoc-form">
            <fieldset>
                <table>

                </table>
            </fieldset>
            <div class="button-panel">
                <input type="submit" name="accept" class="accept" value="Accept">
                <a href="#" class="edit-form"><span class="value">Edit</span></a>
                <a href="#" class="cancel-dialog">Cancel</a>
            </div>
        </form>
    </div>
</script>

<script type="text/x-template" title="adhocworkflows-inputfield">
    <tr>
        <td class="field-name">
            {name}
        </td>
        <td id="{id}" class="value">
        </td>
    </tr>
</script>

<script type="text/x-template" title="adhocworkflows-inputfield-text">
    <span class="value">{value}</span>
    <input name="{id}" type="text" class="text" value="{value}"/>
</script>

<script type="text/x-template" title="adhocworkflows-inputfield-user">
    <span class="user value" title="{value}">{value}</span>
    <input  type="text"
            class="text autocomplete-user"
            name="{id}"
            data-max="10"
            data-template="{username}"
            data-none-message="No matching user found"
            placeholder="Assign to..."
            value="{value}"/>
    <div class="usersdropdown aui-dd-parent">
        <a href="" class="aui-dd-trigger" style="display:none;"></a>
        <ul class="aui-dropdown aui-dropdown-left">
        </ul>
    </div>
</script>

<script type="text/x-template" title="adhocworkflows-inputfield-decorated-user">
    <img src="{user.pictureUrl}" title="{user.fullName}">
    <span>{user.fullName}</span>
</script>


<script type="text/x-template" title="adhocworkflows-inputfield-list">
    <span class="value">
        {value}
    </span>
    <select name="{id}">
    </select>
</script>

<script type="text/x-template" title="adhocworkflows-inputfield-list-option">
    <option {selected}>{option}</option>
</script>

    <ul id="assistive-skip-links" class="assistive">
	<li><a href="\#title-heading">Skip to content</a></li>
	<li><a href="#breadcrumbs">Skip to breadcrumbs</a></li>
	<li><a href="#header-menu-bar">Skip to header menu</a></li>
	<li><a href="#navigation">Skip to action menu</a></li>
	<li><a href="#quick-search-query">Skip to quick search</a></li>
</ul>
<div id="brikit-designer-message"></div>
<div id="needs-page-reload" style="display:none"><span class="needs-page-reload">Required: <a class="aui-button aui-button-link aui-button-subtle" href="/display/HDF5/Introduction+to+HDF5?reload=true">page refresh</a> <span class="aui-lozenge aui-lozenge-subtle countdown">5</span></div>
<!--[if lt IE 8]> 		<div id="page" class="lt-ie10 lt-ie9 lt-ie8">	<![endif]-->
<!--[if IE 8]>    		<div id="page" class="lt-ie10 lt-ie9"> 			<![endif]-->
<!--[if IE 9]>    		<div id="page" class="lt-ie10"> 				<![endif]-->
<!--[if gt IE 9]><!--> 	<div id="page"> 								<!--<![endif]-->
	<div id="full-height-container">
		<div id="header-precursor">
			<div class="cell">
				
				    																</div>
		</div>
				<div id="header-hide-on-load" style="position:absolute;top:-41px;">
			    





<header id="header" role="banner">
    <nav class="aui-header aui-dropdown2-trigger-group" role="navigation"><div class="aui-header-inner"><div class="aui-header-before"><a class=" aui-dropdown2-trigger app-switcher-trigger" aria-owns="app-switcher" aria-controls="app-switcher" aria-haspopup="true" data-aui-trigger href="#app-switcher"><span class="aui-icon aui-icon-small aui-iconfont-appswitcher">Linked Applications</span></a><div id="app-switcher" class="aui-dropdown2 aui-style-default"><div class="app-switcher-loading">Loading&hellip;</div></div><script>
            (function (NL) {
                var initialise = function () {
                    // For some milestones of AUI, the atlassian soy namespace was renamed to aui. Handle that here by ensuring that window.atlassian is defined.
                    window.atlassian = window.atlassian || window.aui;
                    new NL.AppSwitcher({
                        dropdownContents: '#app-switcher'
                    });
                };
                if (NL.AppSwitcher) {
                    initialise();
                } else {
                    NL.onInit = initialise;
                }
            }(window.NL = (window.NL || {})));
            window.NL.environment = {isUserAdmin: false, isAppSuggestionAvailable: false, isSiteAdminUser: false};</script></div><div class="aui-header-primary"><h1 id="logo" class="aui-header-logo aui-header-logo-confluence"><a href="/"><span class="aui-header-logo-device">Confluence</span></a></h1><ul class="aui-nav">
                            <li>
            
        
         

<a  id="space-directory-link" href="/spacedirectory/view.action"  class=" aui-nav-imagelink"   title="Spaces">
            <span>Spaces</span>
    </a>
        </li>
                                        <li class="aui-buttons">
            </li>
    </ul>
</div><div class="aui-header-secondary"><ul class="aui-nav">
                        <li>
        <form id="quick-search" class="aui-quicksearch dont-default-focus header-quicksearch" action="/dosearchsite.action" method="get"><fieldset><label for="quick-search-query" class="assistive">Quick Search</label><input id="quick-search-query" class="text app-search search quick-search-query" type="text" accessKey="q" autocomplete="off" name="queryString" title="Quick Search" placeholder="Search" /><input id="quick-search-submit" class="quick-search-submit" type="submit" value="Search"/><div class="aui-dd-parent quick-nav-drop-down"></div></fieldset></form>
    </li>
        <li>
            
        <a id="help-menu-link" class="aui-nav-link aui-dropdown2-trigger" href="#" aria-haspopup="true" aria-owns="help-menu-link-content" title="Help">
        <span class="aui-icon aui-icon-small aui-iconfont-help">Help</span>
    </a>
    <nav id="help-menu-link-content" class="aui-dropdown2 aui-style-default" aria-hidden="true">
                    <div class="aui-dropdown2-section">
                                <ul  id="help-menu-link-leading" class="aui-list-truncate section-leading first">
                                            <li>
        
             

<a  id="confluence-help-link" href="https://docs.atlassian.com/confluence/docs-59/Getting+Help+And+Support" class="    "      title="Visit the Confluence documentation home"  target="_blank"
>
        Online Help
</a>
</li>
                                            <li>
    
                 

<a  id="keyboard-shortcuts-link" href="#" class="    "      title="View available keyboard shortcuts" >
        Keyboard Shortcuts
</a>
</li>
                                            <li>
    
             

<a  id="feed-builder-link" href="/dashboard/configurerssfeed.action" class="    "      title="Create your custom RSS feed." >
        Feed Builder
</a>
</li>
                                            <li>
    
             

<a  id="whats-new-menu-link" href="https://confluence.atlassian.com/display/DOC/Confluence+5.9+Release+Notes" class="    "      title="" >
        What’s new
</a>
</li>
                                            <li>
    
                 

<a  id="gadget-directory-link" href="#" class="   user-item administration-link "      title="Browse gadgets provided by Confluence" >
        Available Gadgets
</a>
</li>
                                            <li>
    
                 

<a  id="brikit-learn-theme-press-link" href="#" class="    "      title="Brief video tours" >
        Theme Press
</a>
</li>
                                            <li>
    
             

<a  id="confluence-about-link" href="/aboutconfluencepage.action" class="    "      title="Get more information about Confluence" >
        About Confluence
</a>
</li>
                                    </ul>
            </div>
            </nav>
    
    </li>
        <li>
                
    
    </li>
        <li>
            
    </li>
        <li>
                                            <li>
        
             

<a  id="login-link" href="/login.action?os_destination=%2Fdisplay%2FHDF5%2FIntroduction%2Bto%2BHDF5" class="   user-item login-link "      title="" >
        Log in
</a>
</li>
                        
    </li>
    </ul>
</div></div><!-- .aui-header-inner--></nav><!-- .aui-header -->
    <br class="clear">
</header>
    
		</div>

		
				<div class="ia-splitter">
					<div class="ia-splitter-left">
						<div class="ia-fixed-sidebar">
														
							<div class="acs-side-bar ia-scrollable-section"><div class="acs-side-bar-space-info tipsy-enabled" data-configure-tooltip="Edit space details"><div class="avatar"><div class="space-logo" data-key="HDF5" data-name="HDF5" data-entity-type="confluence.space"><div class="avatar-img-container"><div class="avatar-img-wrapper"><a href="/display/HDF5/HDF5" title="HDF5"><img class="avatar-img" src="/download/attachments/425986/global.logo?version=25&amp;modificationDate=1466971937880&amp;api=v2" alt="HDF5"></a></div></div></div></div><div class="space-information-container"><div class="name"><a href="/display/HDF5/HDF5" title="HDF5">HDF5</a></div><div class="flyout-handle icon"></div><div class="favourite-space-icon"><button title="Add to my spaces" id="space-favourite-add" class="space-favourite aui-icon aui-icon-small aui-iconfont-unstar"></button><button class=" space-favourite-hidden  space-favourite aui-icon aui-icon-small aui-iconfont-star" id="space-favourite-remove" title="Remove from my spaces"></button></div></div></div><div class="acs-side-bar-content"><div class="acs-nav-wrapper"><div class="acs-nav" data-has-create-permission="false" data-quick-links-state="null" data-nav-type="page-tree"><div class="acs-nav-sections"><div class="main-links-section "><ul class="acs-nav-list"><li class="acs-nav-item wiki current-item"data-collector-key="spacebar-pages"><a class="acs-nav-item-link tipsy-enabled" href="/collector/pages.action?key=HDF5" data-collapsed-tooltip="Pages"><span class="icon"></span><span class="acs-nav-item-label">Pages</span></a></li><li class="acs-nav-item blog"data-collector-key="spacebar-blogs"><a class="acs-nav-item-link tipsy-enabled" href="/pages/viewrecentblogposts.action?key=HDF5" data-collapsed-tooltip="Blog"><span class="icon"></span><span class="acs-nav-item-label">Blog</span></a></li></ul></div><div class="quick-links-wrapper"></div></div></div></div><div class="ia-secondary-container tipsy-enabled" data-tree-type="page-tree"><div class="ia-secondary-header"><h5 class="ia-secondary-header-title page-tree"><span class="icon"></span><span class="label">Page tree</span></h5></div><div class="ia-secondary-content">


<div class="plugin_pagetree">

        
        
    <ul class="plugin_pagetree_children_list plugin_pagetree_children_list_noleftspace">
        <div class="plugin_pagetree_children">
        </div>
    </ul>

    <fieldset class="hidden">
        <input type="hidden" name="treeId" value="">
        <input type="hidden" name="treeRequestId" value="/plugins/pagetree/naturalchildren.action?decorator=none&amp;excerpt=false&amp;sort=position&amp;reverse=false&amp;disableLinks=false&amp;expandCurrent=true">
        <input type="hidden" name="treePageId" value="50078525">

        <input type="hidden" name="noRoot" value="false">
        <input type="hidden" name="rootPageId" value="48803533">

        <input type="hidden" name="rootPage" value="">
        <input type="hidden" name="startDepth" value="0">
        <input type="hidden" name="spaceKey" value="HDF5" >

        <input type="hidden" name="i18n-pagetree.loading" value="Loading...">
        <input type="hidden" name="i18n-pagetree.error.permission" value="Unable to load page tree. It seems that you do not have permission to view the root page.">
        <input type="hidden" name="i18n-pagetree.eeror.general" value="There was a problem retrieving the page tree. Please check the server log file for more information.">
        <input type="hidden" name="loginUrl" value="/login.action?os_destination=%2Fpages%2Fviewpage.action%3FspaceKey%3DHDF5%26title%3DIntroduction%2Bto%2BHDF5&amp;permissionViolation=true">
        <input type="hidden" name="mobile" value="false">

                <fieldset class="hidden">
                                                <input type="hidden" name="ancestorId" value="48804307">
                                    <input type="hidden" name="ancestorId" value="48803533">
                                    </fieldset>
    </fieldset>
</div>
</div></div></div><div class="hidden"><a href="/collector/pages.action?key=HDF5" id="space-pages-link"></a><script type="text/x-template" title="logo-config-content"><h2>Space Details</h2><div class="personal-space-logo-hint">Your profile picture is used as the logo for your personal space. <a href="/users/profile/editmyprofilepicture.action" target="_blank">Change your profile picture</a>.</div></script></div></div><div class="space-tools-section"><div id="space-tools-menu-additional-items" class="hidden"><div data-label="Browse pages" data-class="" data-href="/pages/reorderpages.action?key=HDF5">Browse pages</div></div><button id="space-tools-menu-trigger" class=" aui-dropdown2-trigger aui-button aui-button-subtle tipsy-enabled" aria-owns="space-tools-menu" aria-controls="space-tools-menu" aria-haspopup="true" data-aui-trigger><span class="aui-icon aui-icon-small aui-iconfont-configure">Configure</span><span class="aui-button-label">Space tools</span><span class="icon aui-icon-dropdown"></span></button><div id="space-tools-menu" class="aui-dropdown2 aui-style-default" data-aui-alignment="top left"></div><a class="expand-collapse-trigger"></a></div>
					
													</div>
					</div><!-- .ia-splitter-left -->
										<!-- \#header -->

					
										    
					
										
					<div class="brikit-toolbar  normal " style="display:none;">
	
    <div id="navigation" class="content-navigation view">
                    <ul class="ajs-menu-bar">
                                                                    <li class="ajs-button normal">

        
            
                                            
     

    
    <a  id="adhocWorkflowsInfoBanner" href="#" rel="nofollow" class="aui-button aui-button-subtle hidden workflow-info-brikit"   title="Workflow">
                    <img alt="Workflow Info" src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB2aWV3Qm94PSIwIDAgOTkuODkgMTQyLjMzIj4KCTx0aXRsZT5Xb3JrZmxvdzwvdGl0bGU+Cgk8cGF0aCBkPSJNNzEuMTcsNDkuOTRhMjEuNzcsMjEuNzcsMCwwLDAtNC42Ny41M0w0OS40MSwzMy4zOGEyMSwyMSwwLDAsMCwuNTMtNC42NkEyMS4yOCwyMS4yOCwwLDEsMCwzMy4zOCw0OS40MWwxNy4wOSwxNy4xYTIwLjc1LDIwLjc1LDAsMCwwLDAsOS4zMkwzMy4zOCw5Mi45MmEyMS4yOCwyMS4yOCwwLDEsMCwxNiwxNkw2Ni41LDkxLjg2YTIxLjIyLDIxLjIyLDAsMSwwLDQuNjctNDEuOTJaIiBzdHlsZT0iZmlsbDojZmZmO3N0cm9rZTojZmZmO3N0cm9rZS1taXRlcmxpbWl0OjEwO3N0cm9rZS13aWR0aDoxNXB4Ii8+Cgk8cGF0aCBkPSJNNzEuMTYsNTBBMjEuMjMsMjEuMjMsMCwwLDAsNDkuOTQsNzEuMjZhMjEuNywyMS43LDAsMCwwLC41Miw0LjY3TDM4LjEzLDg4LjI2QTI3LjU5LDI3LjU5LDAsMCwxLDU0LjQ1LDEwNGwxMi0xMmEyMS42NywyMS42NywwLDAsMCw0LjY2LjUxLDIxLjIyLDIxLjIyLDAsMSwwLDAtNDIuNDRabTUuNzYsMzEuNTFoMGwtLjQ0LjIzTDc2LDgybC0uNDMuMTljLS4yNi4xMS0uNTMuMi0uOC4yOWwtLjM2LjExLS43My4xOS0uMjQsMGMtLjMyLjA3LS42NS4xMi0xLC4xNmwtLjI3LDBjLS4zNiwwLS43MS4wNi0xLjA3LjA2YTExLjgxLDExLjgxLDAsMCwxLTExLjc5LTExLjhjMC0uMzUsMC0uNzEuMDYtMS4wNmwwLS4yN2E4LDgsMCwwLDEsLjE1LTFjMC0uMDgsMC0uMTcsMC0uMjUuMDYtLjI0LjEyLS40OC4xOS0uNzFzLjA3LS4yNi4xMS0uMzguMTgtLjUzLjI5LS43OS4xMy0uMjkuMi0uNDQuMTMtLjI4LjItLjQybC4yMy0uNDVoMGExMS43OSwxMS43OSwwLDEsMSwxNiwxNloiIHN0eWxlPSJmaWxsOiM3MTcwNzAiLz4KCTxwYXRoIGQ9Ik02MC43OSw5Ny42OEEzNi4wNywzNi4wNywwLDAsMCw0NC41NSw4MS44NGwtNi40Miw2LjQyQTI3LjU5LDI3LjU5LDAsMCwxLDU0LjQ1LDEwNFoiIHN0eWxlPSJmaWxsOiM3MTcwNzAiLz4KCTxwYXRoIGQ9Ik0yOC43Miw5Mi40OGEyMS4yMywyMS4yMywwLDEsMCwyMS4yMiwyMS4yM0EyMS4yMywyMS4yMywwLDAsMCwyOC43Miw5Mi40OFptMCwzM2ExMS43OSwxMS43OSwwLDEsMSwxMS43OS0xMS43OUExMS44LDExLjgsMCwwLDEsMjguNzIsMTI1LjVaIiBzdHlsZT0iZmlsbDojNzE3MDcwIi8+Cgk8cGF0aCBkPSJNNDkuNDIsMzMuNDlhMjEuMjIsMjEuMjIsMCwxLDAtMTYsMTZsMTIsMTIuMDZhMjcuNTQsMjcuNTQsMCwwLDEsMTYtMTZaTTE2LjkzLDI4LjgyQTExLjc5LDExLjc5LDAsMCwxLDM5LDIzLjA3aDBjLjA3LjE0LjE0LjI5LjIyLjQzbC4yMi40NS4xOC40MmMuMTEuMjYuMjEuNTMuMy44LDAsLjEyLjA3LjI1LjExLjM3cy4xMy40OC4xOC43MmExLjgzLDEuODMsMCwwLDEsLjA2LjI1Yy4wNy4zMi4xMS42NS4xNSwxbDAsLjI3YzAsLjM1LDAsLjcsMCwxLjA2QTExLjgsMTEuOCwwLDAsMSwyOC43Miw0MC42MWMtLjM2LDAtLjcxLDAtMS4wNiwwbC0uMjcsMGMtLjMzLDAtLjY2LS4wOC0xLS4xNWwtLjI0LS4wNS0uNzMtLjE5TDI1LjA3LDQwYy0uMjctLjA5LS41NC0uMTktLjgtLjNsLS40MS0uMTgtLjQ2LS4yMkwyMywzOS4xMUExMS43OSwxMS43OSwwLDAsMSwxNi45MywyOC44MloiIHN0eWxlPSJmaWxsOiM3MTcwNzAiLz4KCTxwYXRoIGQ9Ik02MS40Nyw0NS41NGwtNi4zOC02LjM4YTM2LDM2LDAsMCwwLTE2LDE2bDYuMzgsNi4zN0EyNy41NSwyNy41NSwwLDAsMSw2MS40Nyw0NS41NFoiIHN0eWxlPSJmaWxsOiM3MTcwNzAiLz4KCjwvc3ZnPg==" height="16" width="16" title="Workflow Info">
                <span>
                        Workflow Info
        </span>    </a>
</li>
                    
        <li class="normal ajs-menu-item">
        <a id="action-menu-link" class="action aui-dropdown2-trigger-arrowless aui-button aui-button-subtle ajs-menu-title aui-dropdown2-trigger" href="#" aria-haspopup="true" aria-owns="action-menu" data-container="#navigation">
            <span>
                                    <span class="aui-icon aui-icon-small aui-iconfont-more"></span>
                                
            </span>
        </a>         <div id="action-menu" class="aui-dropdown2 aui-style-default" aria-hidden="true">
                            <div class="aui-dropdown2-section">
                    <ul  id="action-menu-primary"                         class="section-primary first">
                                                    <li>

    
        
                                            
     

    
    <a  id="view-attachments-link" href="/pages/viewpageattachments.action?pageId=50078525" rel="nofollow" class="action-view-attachments"  accessKey="t"  title="View Attachments">
                <span>
                        A<u>t</u>tachments (12)
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="action-view-history-link" href="/pages/viewpreviousversions.action?pageId=50078525" rel="nofollow" class="action-view-history"   title="">
                <span>
                        Page History
        </span>    </a>
</li>
                                        </ul>
                </div>
                            <div class="aui-dropdown2-section">
                    <ul  id="action-menu-secondary"                         class="section-secondary">
                                                    <li>

    
        
                                            
     

    
    <a  id="view-page-info-link" href="/pages/viewinfo.action?pageId=50078525" rel="nofollow" class="action-view-info"   title="">
                <span>
                        Page Information
        </span>    </a>
</li>
                                                <li>

    
            
                                            
     

    
    <a  id="view-resolved-comments" href="#" rel="nofollow" class=""   title="">
                <span>
                        Resolved comments
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="link-to-page-link" href="/pages/viewinfo.action?pageId=50078525" rel="nofollow" class=""   title="Link to this Page">
                <span>
                        Link to this Page…
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="view-in-hierarchy-link" href="/pages/listpages-dirview.action?key=HDF5&amp;openId=50078525#selectedPageInHierarchy" rel="nofollow" class=""   title="">
                <span>
                        View in Hierarchy
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="action-view-source-link" href="/plugins/viewsource/viewpagesrc.action?pageId=50078525" rel="nofollow" class="action-view-source popup-link"   title="">
                <span>
                        View Source
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="action-export-pdf-link" href="/spaces/flyingpdf/pdfpageexport.action?pageId=50078525" rel="nofollow" class=""   title="">
                <span>
                        Export to PDF
        </span>    </a>
</li>
                                                <li>

    
        
                                            
     

    
    <a  id="action-export-word-link" href="/exportword?pageId=50078525" rel="nofollow" class="action-export-word"   title="">
                <span>
                        Export to Word
        </span>    </a>
</li>
                                        </ul>
                </div>
                    </div>
    </li>
            </ul>
    </div>

    
</div>

										<div id="main" class=" aui-page-panel brikit-canvas">

																		
						
						
							<div class="brikit-container-backdrop brikit-header-backdrop " >
		<div class="brikit-container brikit-header-container">
	    	<div  id="main-header"  class="brikit-container-content brikit-header">
													<div 				 class="brikit-header-content "
				 data-page-id="48805863">
				<div class=" brikit-architect-page-container    " id="content-layer-699401031" data-content-layer="699401031" data-name=""
	style="		 height:false; 																	"
	><div class=" brikit-architect-table "
			><div class=" brikit-architect-container-content " style="		 height:false; 																										"
			><div class="brikit-content-layer-table"
				><div class="brikit-content-layer-table-row designable-element">
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-699401033" data-content-column="699401033"
	style="
		 width:; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-699401032" data-content-block="699401032"  style="
																	"><p><style>
.ia-fixed-sidebar,
.brikit-toolbar,
#header {
    display:none;
    height:0px;
    width:0px;
}
</style></p><a name="toppage"></a>
<script>
$(document).ready(function(e) {   
$(".hdf-page-title").prepend($('meta[name=ajs-page-title]').attr("content"));
var ShowC = function() {  
  $(".hdf-togglebox").addClass("hdf-togglebox-hidden");
  $(".hdf-togglebutton").removeClass("hdf-toggled-on");  
  $(".hdf-togglebutton.hdf-c").addClass("hdf-toggled-on");  
  $(".hdf-togglebox.hdf-c").removeClass("hdf-togglebox-hidden");  
};
var ShowFortran = function() {
  $(".hdf-togglebox").addClass("hdf-togglebox-hidden");   
  $(".hdf-togglebutton").removeClass("hdf-toggled-on");  
  $(".hdf-togglebutton.hdf-fortran").addClass("hdf-toggled-on");  
  $(".hdf-togglebox.hdf-fortran").removeClass("hdf-togglebox-hidden");
};
var ShowCXX = function() {
  $(".hdf-togglebox").addClass("hdf-togglebox-hidden");  
  $(".hdf-togglebutton").removeClass("hdf-toggled-on");  
  $(".hdf-togglebutton.hdf-cxx").addClass("hdf-toggled-on");  
  $(".hdf-togglebox.hdf-cxx").removeClass("hdf-togglebox-hidden");  
};
var ShowJava = function() {
  $(".hdf-togglebox").addClass("hdf-togglebox-hidden");  
  $(".hdf-togglebutton").removeClass("hdf-toggled-on");  
  $(".hdf-togglebutton.hdf-java").addClass("hdf-toggled-on");  
  $(".hdf-togglebox.hdf-java").removeClass("hdf-togglebox-hidden");    
};
$(".hdf-fortran.hdf-togglebutton").click(ShowFortran);
$(".hdf-cxx.hdf-togglebutton").click(ShowCXX);
$(".hdf-c.hdf-togglebutton").click(ShowC);
$(".hdf-java.hdf-togglebutton").click(ShowJava);
  $(".expandable").prepend('<div class="obutton"><i class="fa fa-arrows-alt"></i></div>');
  $(".expandable").prepend('<div class="xbutton"><i class="fa fa-chevron-down"></i></div>');
  $(".rm_pagetree_col").prepend('<div class="hdf-sidebar-button"><i class="hdf-sidebar-button-icon fa fa-bars" aria-hidden="true"></i><span class="hdf-sidebar-button-text">Contents</span></div>');
  $(".heatmap li:contains('faq')").css("display", "none");
  $(".heatmap li:contains('kb-article')").css("display", "none");
  var Collapse = function(){    
    $(".sidebutton").toggleClass("collapsed")
    $(".rm_pagetree_col").toggleClass("collapsed")    
    $(".rm_syntax_col").toggleClass("collapsed")
    $(".rm_proto_col").toggleClass("collapsed")
    $(".brikit-content-layer").toggleClass("collapsed")
  };  
  $(".sidebutton").click(Collapse);
  $(".hdf-sidebar-button").click(Collapse); 
  var Expand = function(){  
    $(".expandable").removeClass("hdf_fullscreen");    
    $('.xbutton').removeClass('showxbutton');       
    $(".obutton").removeClass("hideobutton");
    $(this).parent().addClass("hdf_fullscreen");
    $(".brikit").addClass("hdf_locked");
    $(this).parent().children(".xbutton").addClass("showxbutton");
    $(this).addClass("hideobutton");
  };
  var Shrink = function(){
    $('.hdf_fullscreen').removeClass('hdf_fullscreen');     
    $('.xbutton').removeClass('showxbutton');     
    $(".obutton").removeClass("hideobutton");
    $(".brikit").removeClass("hdf_locked");
  };
  $(".obutton").click(Expand);
  $('.xbutton').click(Shrink);
  document.onkeydown = (function(evt) {
    evt = evt || window.event;
    var isEscape = false;
    if ("key" in evt) {
      isEscape = (evt.key == "Escape" || evt.key == "Esc");
    } else {
      isEscape = (evt.keyCode == 27);
    }
    if (isEscape) {
      Shrink();
    }
  });
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.brikit-menu-top-level.brikit-menu').hasClass('hdf-sticky-menu') ) {
    $('.brikit-menu-top-level.brikit-menu').addClass('hdf-sticky-menu');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.brikit-menu-top-level.brikit-menu').removeClass('hdf-sticky-menu');    
  }
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.hdf-sidebar-button').hasClass('hdf-sticky-sidebar-button') ) {
    $('.hdf-sidebar-button').addClass('hdf-sticky-sidebar-button');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.hdf-sidebar-button').removeClass('hdf-sticky-sidebar-button');    
  }
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.hdf-rm-navbar').hasClass('sticky') ) {
    $('.hdf-rm-navbar').addClass('sticky');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.hdf-rm-navbar').removeClass('sticky');    
  }
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.hdf-rm-summary-block').hasClass('sticky') ) {
    $('.hdf-rm-summary-block').addClass('sticky');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.hdf-rm-summary-block').removeClass('sticky');    
  }
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.hdf-rm-onecol-content-stack').hasClass('sticky') ) {
    $('.hdf-rm-onecol-content-stack').addClass('sticky');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.hdf-rm-onecol-content-stack').removeClass('sticky');    
  }
});
$(window).scroll(function () {
  if ( $(this).scrollTop() > 80 && !$('.brikit-content-layer').hasClass('sticky') ) {
    $('.brikit-content-layer').addClass('sticky');    
   } else if ( $(this).scrollTop() <= 80 ) {
    $('.brikit-content-layer').removeClass('sticky');    
  }
});

</script>
<link rel="stylesheet" href="https://use.fontawesome.com/f603cf5a9c.css"><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column --></div></div></div></div></div><!-- /.brikit-content-layer-container -->

								<div style="clear:both"></div>
			</div>
			<script type="text/javascript">
	(function ($) {
		$(".brikit-header").append($(".brikit-toolbar.header-toolbar"));
	})(jQuery);
</script>
                    
    
												<div class="brikit-menu" style="display:none">
			<div class=" brikit-architect-page-container    " id="content-layer-1" data-content-layer="1" data-name=""
	style="		 height:false; 																	"
	><div class=" brikit-architect-table "
			><div class=" brikit-architect-container-content " style="		 height:false; 																										"
			><div class="brikit-content-layer-table"
				><div class="brikit-content-layer-table-row designable-element">
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-11" data-content-column="11"
	style="
		 width:100.00002%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-111" data-content-block="111"  style="
																	"><ul><li><a href="/display/support/Documentation">Documentation</a></li><li><a href="/display/knowledge">Knowledge</a></li><li><a href="/display/support/The+HDF+Help+Desk">Help Desk</a></li><li><a href="/display/support/Downloads">Downloads</a></li></ul><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column --></div></div></div></div></div><!-- /.brikit-content-layer-container -->

		</div>
	<div id="brikit-menu-template" class="brikit-menu-top-level" style="display:none">
	<nav class="aui-navgroup aui-navgroup-horizontal">
	    <div class="aui-navgroup-inner">
	        <div class="aui-navgroup-primary"></div><!-- .aui-navgroup-primary -->
	        <div class="aui-navgroup-secondary"></div><!-- .aui-navgroup-secondary -->
	    </div><!-- .aui-navgroup-inner -->
	</nav>
</div>
<div class="aui-dropdown2 aui-style-default brikit-menu-dropdown" id="brikit-dropdown-template" style="display:none"></div>
<div class="aui-dropdown2 brikit-menu-panel" id="brikit-menu-panel-template" style="display:none"></div>
											<a class="brikit-logo" href="/display/support"><img src="/plugins/servlet/themepress/brikitservlet/designs/themes/Limelight/images/HDFG-logo.png" alt="logo" border="0"  height="52px"   /></a>
												<div id="brikit-search"></div>
									</div>
		</div>
	</div>


						

						<div id="sidebar-container">
																																</div><!-- \#sidebar-container -->

										<div class="brikit-content-stack">
													<div class="brikit-container-backdrop brikit-title-backdrop false"  style="display: none;" >
		<div class="brikit-container brikit-title-container">
	    	<div  class="brikit-container-content brikit-title">
							<div id="title-heading" class="brikit-page-title pagetitle with-breadcrumbs" style="display:none">
    
	
		        	    

    <a class="assistive" href="#page-metadata-end">Skip to end of metadata</a>
        	<div id="page-metadata-start" class="assistive"></div>
        	        
            <div id="page-metadata-banner"><ul class="banner"><li id="system-content-items" class="noprint"><a href="" title="Unrestricted" id="content-metadata-page-restrictions-hidden" class="hidden"></a><a href="/pages/viewpageattachments.action?pageId=50078525&amp;metadataLink=true" title="12 attachments" id="content-metadata-attachments" class="aui-icon aui-icon-small aui-iconfont-attachment"></a></li><li class="page-metadata-item noprint has-button"  id="content-metadata-jira-wrapper"><a href="" title="" id="content-metadata-jira" class="aui-button aui-button-subtle content-metadata-jira tipsy-disabled hidden"><span>JIRA links</span></a></li></ul></div>
    		    

	<h1 id="title-text" class="with-breadcrumbs">
	    	                    <a href="/display/HDF5/Introduction+to+HDF5">Introduction to HDF5</a>
    	    	</h1>
</div>

	<div class="brikit-page-metadata"></div>
									</div>
		</div>
	</div>

																										
    

                                




            
    	

	
	

							                    
    
	
    
    
        
    
    
                    
    


	    

    


	    

		<meta name="ajs-mode" content="view">
			
	
	    

	    


	    

	    

			
	
	    

		
		
	    

<div id="content" class="page view">
    


<div id="action-messages">
                        </div>



        <script type="text/x-template" title="searchResultsGrid">
    <table class="aui">
        <thead>
            <tr class="header">
                <th class="search-result-title">Page Title</th>
                <th class="search-result-space">Space</th>
                <th class="search-result-date">Updated</th>
            </tr>
        </thead>
    </table>
</script>
<script type="text/x-template" title="searchResultsGridCount">
    <p class="search-result-count">{0}</p>
</script>
<script type="text/x-template" title="searchResultsGridRow">
    <tr class="search-result">
        <td class="search-result-title"><a href="{1}" class="content-type-{2}"><span>{0}</span></a></td>
        <td class="search-result-space"><a class="space" href="/display/{4}/" title="{3}">{3}</a></td>
        <td class="search-result-date"><span class="date" title="{6}">{5}</span></td>
    </tr>
</script>
        
    
            

			<script type="text/javascript">
		ThemePress.colors.primary 		= ThemePress.html.toRGB("#151515");
		ThemePress.colors.secondary 	= ThemePress.html.toRGB("#67A155");
		ThemePress.colors.tertiary 		= ThemePress.html.toRGB("#6176A8");
		ThemePress.colors.dark 			= ThemePress.html.toRGB("#3E3F40");
		ThemePress.colors.medium 		= ThemePress.html.toRGB("#808284");
		ThemePress.colors.light 		= ThemePress.html.toRGB("#C8FFBA");
		ThemePress.colors.darkgray 		= ThemePress.html.toRGB("#808284");
		ThemePress.colors.mediumgray 	= ThemePress.html.toRGB("#E0E0E0");
		ThemePress.colors.lightgray 	= ThemePress.html.toRGB("#F5F5F5");
		ThemePress.colors.white 		= ThemePress.html.toRGB("#FFFFFF");
	
		if (ThemePress.colors.primary) 		ThemePress.reverseColors[ThemePress.colors.primary.toLowerCase()] 		= "\$primaryColor";
		if (ThemePress.colors.secondary)  	ThemePress.reverseColors[ThemePress.colors.secondary.toLowerCase()] 	= "\$secondaryColor";
		if (ThemePress.colors.tertiary)   	ThemePress.reverseColors[ThemePress.colors.tertiary.toLowerCase()] 		= "\$tertiaryColor";
		if (ThemePress.colors.dark) 	  	ThemePress.reverseColors[ThemePress.colors.dark.toLowerCase()] 			= "\$darkColor";
		if (ThemePress.colors.medium) 	  	ThemePress.reverseColors[ThemePress.colors.medium.toLowerCase()] 		= "\$mediumColor";
		if (ThemePress.colors.light) 	  	ThemePress.reverseColors[ThemePress.colors.light.toLowerCase()] 		= "\$lightColor";
		if (ThemePress.colors.darkgray)   	ThemePress.reverseColors[ThemePress.colors.darkgray.toLowerCase()] 		= "\$darkGrayColor";
		if (ThemePress.colors.mediumgray) 	ThemePress.reverseColors[ThemePress.colors.mediumgray.toLowerCase()] 	= "\$mediumGrayColor";
		if (ThemePress.colors.lightgray)  	ThemePress.reverseColors[ThemePress.colors.lightgray.toLowerCase()] 	= "\$lightGrayColor";
		if (ThemePress.colors.white) 	 	ThemePress.reverseColors[ThemePress.colors.white.toLowerCase()] 		= "\$whiteColor";
	</script>

        
                            
    

                    

        
		<div id="page-metadata-hide" style="display:none">
                

    <a class="assistive" href="#page-metadata-start">Go to start of metadata</a>
            <div id="page-metadata-end" class="assistive"></div>

            <a href="#page-metadata-end" class="assistive">Skip to end of metadata</a>
<div id="page-metadata-start" class="assistive"></div>

    <div class="page-metadata">
        <ul>
            <li class="page-metadata-modification-info">
                
        
    
        
    
        
            
            Created by <span class='author'>     <a href="    /display/~bljones
"
                       class="url fn"
                            >Barbara Jones</a></span>, last modified on <a class='last-modified' title='Show changes' href='/pages/diffpagesbyversion.action?pageId=50078525&amp;selectedPageVersions=56&amp;selectedPageVersions=57'>Feb 08, 2018</a>
                </li>
        </ul>
    </div>


<a href="#page-metadata-start" class="assistive">Go to start of metadata</a>
<div id="page-metadata-end" class="assistive"></div>
		</div>

        
                                		    

				<div id="main-content" class="wiki-content brikit-draggable-area brikit-content-layers ">
		
	
				

				
	
			<div class=" brikit-container-backdrop brikit-content-layer-backdrop brikit-content-layer    " id="content-layer-0" data-content-layer="0" data-name=""
	style="		 height:false; 																	"
	><div class=" brikit-container brikit-content-layer-container "
			><div class=" brikit-container-content brikit-layer " style="		 height:false; 																										"
			><div class="brikit-content-layer-table"
				><div class="brikit-content-layer-table-row designable-element">
	<div class="brikit-content-column brikit-content-column-normal designable-element
					from-layout
					mobile-hide
		" id="content-column-0" data-content-column="0"
	style="
		 width:20%; 	 height:false; 						background-color:#E0E0E0;
								">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element   position-top     " id="content-block-111" data-content-block="111"  style="
					 padding:10px; 			background-color:rgba(0,0,0,0);
								 border-width: 0px; 				"><h3 style="text-align: left;" id="IntroductiontoHDF5-true"><a class="space-name-macro-link" data-key="HDF5" href="/display/"><span class="space-name-macro-name" data-name="HDF5"></span></a></h3><p style="text-align: left;">


<div class="plugin_pagetree">

        
                <div>
            <span class="plugin_pagetree_status hidden">Collapse all</span>
            <div class="plugin_pagetree_expandcollapse">
                <a class="plugin_pagetree_expandall" href="#">Expand all</a>&nbsp;&nbsp;
                <a class="plugin_pagetree_collapseall" href="#">Collapse all</a>
            </div>
        </div>
    
    <ul class="plugin_pagetree_children_list plugin_pagetree_children_list_noleftspace">
        <div class="plugin_pagetree_children">
        </div>
    </ul>

    <fieldset class="hidden">
        <input type="hidden" name="treeId" value="">
        <input type="hidden" name="treeRequestId" value="/plugins/pagetree/naturalchildren.action?decorator=none&amp;excerpt=false&amp;sort=position&amp;reverse=false&amp;disableLinks=false&amp;expandCurrent=false">
        <input type="hidden" name="treePageId" value="50078525">

        <input type="hidden" name="noRoot" value="false">
        <input type="hidden" name="rootPageId" value="48803533">

        <input type="hidden" name="rootPage" value="">
        <input type="hidden" name="startDepth" value="0">
        <input type="hidden" name="spaceKey" value="HDF5" >

        <input type="hidden" name="i18n-pagetree.loading" value="Loading...">
        <input type="hidden" name="i18n-pagetree.error.permission" value="Unable to load page tree. It seems that you do not have permission to view the root page.">
        <input type="hidden" name="i18n-pagetree.eeror.general" value="There was a problem retrieving the page tree. Please check the server log file for more information.">
        <input type="hidden" name="loginUrl" value="/login.action?os_destination=%2Fpages%2Fviewpage.action%3FspaceKey%3DHDF5%26title%3DIntroduction%2Bto%2BHDF5&amp;permissionViolation=true">
        <input type="hidden" name="mobile" value="false">

                <fieldset class="hidden">
                                                <input type="hidden" name="ancestorId" value="48804307">
                                    <input type="hidden" name="ancestorId" value="48803533">
                                    </fieldset>
    </fieldset>
</div>

</p><p style="text-align: left;"><script type="text/javascript">
	var addClass = function () {
		jQuery("div.from-layout").addClass("hdf_layout");
	}
			addClass();
	</script>
</p><p style="text-align: left;"><script type="text/javascript">
	var addClass = function () {
		jQuery("#brikit-footer-shim").addClass("rm_hide_shim");
	}
			ThemePress.toFinalize(addClass);
	</script>
</p><p style="text-align: left;"><script type="text/javascript">
	var addClass = function () {
		jQuery(".brikit-content-layers").addClass("rm-content-layers");
	}
			addClass();
	</script>
</p><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column -->
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-0" data-content-column="0"
	style="
		 width:80.0%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-0" data-content-block="0"  style="
																	">
		                
        <ul><li><p><strong><a href="#IntroductiontoHDF5-hdf5desc">HDF5 Description</a></strong></p></li><li><strong><a href="#IntroductiontoHDF5-introprog">Introduction to the HDF5 Programming Model and APIs</a></strong></li></ul><h2 id="IntroductiontoHDF5-hdf5descHDF5Description"><strong><span class="confluence-anchor-link" id="IntroductiontoHDF5-hdf5desc"></span>HDF5 Description</strong></h2><p>HDF5 consists of a <a href="#IntroductiontoHDF5-fileformat"><em>file format</em></a> for storing HDF5 data, a <a href="#IntroductiontoHDF5-datamodel"><em>data model</em></a> for logically organizing and accessing HDF5 data from an application, and the <a href="#IntroductiontoHDF5-software"><em>software</em></a> (libraries, language interfaces, and tools) for working with this format.</p><h3 id="IntroductiontoHDF5-fileformatFileFormat"><strong><span class="confluence-anchor-link" id="IntroductiontoHDF5-fileformat"></span></strong>File Format</h3><p>The HDF5 File Format is defined by and adheres to the HDF5 File Format Specification, which specifies the bit-level organization of an HDF5 file on storage media. <em>In general users do not need to know details about it</em>.</p><h3 id="IntroductiontoHDF5-datamodelDataModel"><strong><span class="confluence-anchor-link" id="IntroductiontoHDF5-datamodel"></span></strong>Data Model    <strong>             </strong></h3><p>The HDF5 Data Model, also known as the HDF5 Abstract (or Logical) Data Model consists of the building blocks for data organization and specification in HDF5.</p><p>An HDF5 file (an object in itself) can be thought of as a container (or group) that holds a variety of heterogeneous data objects (or datasets). The datasets can be images, tables, graphs, and even documents, such as PDF or Excel:</p><p style="margin-left: 30.0px;"><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/fileobj.png?version=1&amp;modificationDate=1517514518882&amp;api=v2" data-image-src="/download/attachments/50078525/fileobj.png?version=1&amp;modificationDate=1517514518882&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078527" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="fileobj.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p>The two primary objects in the HDF5 Data Model are <a href="#IntroductiontoHDF5-group"><em>groups</em></a> and <em><a href="#IntroductiontoHDF5-dataset">datasets</a></em>.</p><p>There are also a variety of other objects in the HDF5 Data Model that support groups and datasets, including <a href="#IntroductiontoHDF5-otherobjs"><em>datatypes</em>, <em>dataspaces</em>, <em>properties </em>and <em>attributes</em></a>.</p><h4 id="IntroductiontoHDF5-groupGroups"><span class="confluence-anchor-link" id="IntroductiontoHDF5-group"></span>Groups</h4><p>HDF5 groups (and links) organize data objects.  Every HDF5 file contains a root group that can contain other groups or be linked to objects in other files.</p><p>          <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/group.png?version=1&amp;modificationDate=1517515131580&amp;api=v2" data-image-src="/download/attachments/50078525/group.png?version=1&amp;modificationDate=1517515131580&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078535" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="group.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span>                                                                                            </p><p style="margin-left: 60.0px;"><sub>There are two groups in the HDF5 file depicted above: Vis and SimOut. Under the Viz group are a variety of images and a table that is shared with the SimOut group. The SimOut group contains a 3-dimensional array, a 2-dimensional array and a link to a 2-dimensional array in another HDF5 file.</sub></p><p>Working with groups and group members is similar in many ways to working with directories and files in UNIX. As with UNIX directories and files, objects in an HDF5 file are often described by giving their full (or absolute) path names.</p><p style="margin-left: 30.0px;"><code>/</code> signifies the root group.</p><p style="margin-left: 30.0px;"><code>/foo</code> signifies a member of the root group called foo.</p><p style="margin-left: 30.0px;"><code>/foo/zoo</code> signifies a member of the group foo, which in turn is a member of the root group.</p><h4 id="IntroductiontoHDF5-datasetDatasets"><span class="confluence-anchor-link" id="IntroductiontoHDF5-dataset"></span>Datasets</h4><p>HDF5 datasets organize and contain the “raw” data values. A dataset consists of metadata that describes the data, in addition to the data itself:</p><p style="margin-left: 30.0px;">     <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/dataset.png?version=1&amp;modificationDate=1517515671633&amp;api=v2" data-image-src="/download/attachments/50078525/dataset.png?version=1&amp;modificationDate=1517515671633&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078547" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="dataset.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span>  </p><p style="margin-left: 60.0px;"><sub>In the picture above, the data is stored as a three dimensional dataset of size 4 x 5 x 6 with an integer datatype. It contains attributes, <em>Time</em> and <em>Pressure</em>, and the dataset is chunked and compressed.</sub></p><p>Datatypes, dataspaces, properties and (optional) attributes are HDF5 objects that describe a dataset. The datatype describes the individual data elements.</p><h4 id="IntroductiontoHDF5-otherobjsDatatypes,Dataspaces,PropertiesandAttributes"><span class="confluence-anchor-link" id="IntroductiontoHDF5-otherobjs"></span>Datatypes, Dataspaces, Properties and Attributes</h4><h5 id="IntroductiontoHDF5-Datatypes"><em>Datatypes</em></h5><p>The datatype describes the individual data elements in a dataset. It provides complete information for data conversion to or from that datatype.      </p><p>       <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/datatype.png?version=1&amp;modificationDate=1517521915894&amp;api=v2" data-image-src="/download/attachments/50078525/datatype.png?version=1&amp;modificationDate=1517521915894&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078597" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="datatype.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span>  </p><p style="margin-left: 30.0px;"><sub>In the dataset depicted above each element of the dataset is a 32-bit integer.</sub></p><p>Datatypes in HDF5 can be grouped into:</p><p style="margin-left: 30.0px;"><strong><em>Pre-Defined Datatypes</em>: </strong>  These are datatypes that are created by HDF5. They are actually opened (and closed) by HDF5 and can have different values from one HDF5 session to the next. There are two types of pre-defined datatypes:</p><ul><li style="list-style-type: none;background-image: none;"><ul><li>Standard datatypes are the same on all platforms and are what you see in an HDF5 file. Their names are of the form H5T_ARCH_BASE where ARCH is an architecture name and BASE is a pro­gramming type name. For example, <code>H5T_IEEE_F32BE</code> indicates a standard Big Endian floating point type.</li></ul></li></ul><ul><li style="list-style-type: none;background-image: none;"><ul><li>Native datatypes are used to simplify memory operations (reading, writing) and are NOT the same on different platforms. For example, <code>H5T_NATIVE_INT</code> indicates an <code>int</code> (C).</li></ul></li></ul><p><em> </em></p><p style="margin-left: 30.0px;"><strong><em>Derived Datatypes:</em>  </strong> These are datatypes that are created or derived from the pre-defined datatypes. An example of a commonly used derived datatype is a <em>string</em> of more than one character. Compound datatypes are also derived types.  A compound datatype can be used to create a simple <em>table</em>, and can also be <em>nested</em>, in which it includes one more other compound datatypes.</p><p style="margin-left: 60.0px;"><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/cmpnddtype.png?version=1&amp;modificationDate=1517522158356&amp;api=v2" data-image-src="/download/attachments/50078525/cmpnddtype.png?version=1&amp;modificationDate=1517522158356&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078604" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="cmpnddtype.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p style="margin-left: 60.0px;"><sub>This is an example of a dataset with a compound datatype. Each element in the dataset consists of a 16-bit integer, a character, a 32-bit integer, and a 2x3x2 array of 32-bit floats (the datatype).  It is a 2-dimensional 5 x 3 array (the dataspace). The datatype should not be confused with the dataspace.</sub></p><h5 id="IntroductiontoHDF5-Dataspaces"><em>Dataspaces</em></h5><p>A dataspace describes the layout of a dataset’s data elements.  It can consist of no elements (NULL), a single element (scalar), or a simple array.          </p><p>                    <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/dataspace1.png?version=1&amp;modificationDate=1517604051328&amp;api=v2" data-image-src="/download/attachments/50078525/dataspace1.png?version=1&amp;modificationDate=1517604051328&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078806" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="dataspace1.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p style="margin-left: 90.0px;"><sub>This image illustrates a dataspace that is an array with dimensions of 5 x 3 and a rank (number of dimensions) of 2.</sub></p><p>A dataspace can have dimensions that are fixed (unchanging) or <em>unlimited</em>, which means they can grow in size (i.e. they are extendible).</p><p>There are two roles of a dataspace:</p><ul><li>It contains the spatial information (logical layout) of a dataset stored in a file. This includes the rank and dimensions of a dataset, which are a permanent part of the dataset definition.</li></ul><ul><li>It describes an application’s data buffers and data elements participating in I/O. In other words, it can be used to select a portion or subset of a dataset.</li></ul><p style="margin-left: 30.0px;">   <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/dataspace.png?version=1&amp;modificationDate=1517603970330&amp;api=v2" data-image-src="/download/attachments/50078525/dataspace.png?version=1&amp;modificationDate=1517603970330&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078805" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="dataspace.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p style="margin-left: 90.0px;"><sub>The dataspace is used to describe both the logical layout of a dataset and a subset of a dataset.</sub></p><h5 id="IntroductiontoHDF5-Properties"><em>Properties</em></h5><p>A property is a characteristic or feature of an HDF5 object. There are default properties which handle the most common needs. These default properties can be modified using the HDF5 Property List API to take advantage of more powerful or unusual features of HDF5 objects.</p><p>For example, the data storage layout property of a dataset is contiguous by default. For better performance, the layout can be modified to be <em>chunked</em> or <em>chunked and compressed</em>:</p><p style="margin-left: 60.0px;"><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" height="250" src="/download/attachments/50078525/properties.png?version=1&amp;modificationDate=1517604231248&amp;api=v2" data-image-src="/download/attachments/50078525/properties.png?version=1&amp;modificationDate=1517604231248&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078809" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="properties.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><h5 id="IntroductiontoHDF5-Attributes"><em>Attributes</em></h5><p>Attributes can optionally be associated with HDF5 objects. They have two parts: a name and a value. Attributes are accessed by opening the object that they are attached so are not independent objects. Typically an attribute is small in size and contains user metadata about the object that it is attached to.</p><p>Attributes look similar to HDF5 datasets in that they have a datatype and dataspace. However, they do not support partial I/O operations, and they cannot be compressed or extended.</p><h3 id="IntroductiontoHDF5-softwareHDF5Software"><strong><span class="confluence-anchor-link" id="IntroductiontoHDF5-software"></span></strong>HDF5 Software</h3><p>The HDF5 software is written in C and includes optional wrappers for C++, FORTRAN (90 and F2003), and Java. The HDF5 binary distribution consists of the HDF5 libraries, include files, command-line utilities, scripts for compiling applications, and example programs.</p><h4 id="IntroductiontoHDF5-HDF5APIsandLibraries">HDF5 APIs and Libraries</h4><p>There are APIs for each type of object in HDF5. For example, all C routines in the HDF5 library begin with a prefix of the form H5*, where * is one or two uppercase letters indicating the type of object on which the function operates:</p><p>            H5A     <strong>A</strong>ttribute Interface</p><p>            H5D     <strong>D</strong>ataset Interface</p><p>            H5F      <strong>F</strong>ile Interface</p><p>The HDF5 High Level APIs simplify many of the steps required to create and access objects, as well as providing templates for storing objects. Following is a list of the High Level APIs:</p><ul><li>HDF5 Lite (H5LT) – simplifies steps in creating datasets and attributes</li><li>HDF5 Image (H5IM) – defines a standard for storing images in HDF5</li><li>HDF5 Table (H5TB) – condenses the steps required to create tables</li><li>HDF5 Dimension Scales (H5DS) – provides a standard for dimension scale storage</li><li>HDF5 Packet Table (H5PT) – provides a standard for storing packet data</li></ul><h4 id="IntroductiontoHDF5-Tools">Tools</h4><p>Useful tools for working with HDF5 files include:</p><p style="margin-left: 30.0px;"><em>h5dump:</em>                      A utility to dump or display the contents of an HDF5 File  </p><p style="margin-left: 30.0px;"><em>h5cc, h5c++, h5fc: </em>      Unix scripts for compiling applications</p><p style="margin-left: 30.0px;"><em>HDFView:</em>                    A java browser to view HDF (HDF4 and HDF5) files  </p><p> </p><h5 id="IntroductiontoHDF5-h5dump:">h5dump:</h5><p>The h5dump utility displays the contents of an HDF5 file in Data Description Language (DDL).Below is an example of h5dump output for an HDF5 file that contains no objects:</p><p style="margin-left: 60.0px;"><code>$ h5dump file.h5</code></p><p style="margin-left: 60.0px;"><code>HDF5 &quot;file.h5&quot; {</code></p><p style="margin-left: 60.0px;"><code>GROUP &quot;/&quot; {</code></p><p style="margin-left: 60.0px;"><code>}</code></p><p style="margin-left: 60.0px;"><code>}</code></p><p>With large files and datasets the output from h5dump can be overwhelming.  There are options that can be used to examine specific parts of an HDF5 file. Some useful h5dump options are included below:</p><p style="margin-left: 60.0px;"><code>-H, --header</code>      Display header information only (no data)</p><p style="margin-left: 60.0px;"><code>-d &lt;name&gt;      </code>Display a dataset with a specified path and name</p><p style="margin-left: 60.0px;"><code>-p</code>                          Display properties</p><p style="margin-left: 60.0px;"><code>-n</code>                          Display the contents of the file</p><h5 id="IntroductiontoHDF5-h5cc,h5fc,h5c++:">h5cc, h5fc, h5c++:</h5><p>The built HDF5 binaries include the h5cc, h5fc, h5c++ compile scripts for compiling applications. When using these scripts there is no need to specify the HDF5 libraries and include files.  Compiler options can be passed to the scripts:</p><p>             <code>  h5cc myprog.c    </code></p><p style="margin-left: 60.0px;"><code> ./a.out</code></p><h5 id="IntroductiontoHDF5-HDFView:">HDFView:</h5><p>The HDFView tool allows browsing of data in HDF (HDF4 and HDF5) files. </p><p> </p><h2 id="IntroductiontoHDF5-introprogIntroductiontotheHDF5ProgrammingModelandAPIs"><strong><span class="confluence-anchor-link" id="IntroductiontoHDF5-introprog"></span>Introduction to the HDF5 Programming Model and APIs</strong></h2><p>The HDF5 Application Programming Interface is extensive, but a few functions do most of the work.</p><p>To introduce the programming model, examples in Python and C are included below. The Python examples use the HDF5 Python APIs (h5py). See the <a href="/display/HDF5/Examples+from+Learning+the+Basics">Examples from &quot;Learning the Basics&quot;</a> page for complete examples that can be downloaded and run for C, FORTRAN, C++, Java and Python.</p><p>The general paradigm for working with objects in HDF5 is to:</p><ul><li>Open the object.</li><li>Access the object.</li><li>Close the object.</li></ul><p><em>The library imposes an order on the operations by argument dependencies.</em> For example, a file must be opened before a dataset because the dataset open call requires a file handle as an argument. Objects can be closed in any order. However, once an object is closed it no longer can be accessed.</p><p>Keep the following in mind when looking at the example programs included in this section:</p><ul><li>C routines begin with the prefix “<code>H5*</code>” where * is a single letter indicating the object on which the operation is to be performed.  FORTRAN routines are similar; they begin with “<code>h5*</code>” and end with “<code>_f</code>”. For example:</li></ul><p>            File Interface:              <code>H5Fopen</code> (C) and <code>h5fopen_f</code> (FORTRAN)</p><p>            Dataset Interface:        <code>H5Dopen</code> (C) and <code>h5dopen_f</code> (FORTRAN)</p><p>            Dataspace interface:   <code>H5Sclose</code> (C) and <code>h5sclose_f</code> (FORTRAN)</p><p style="margin-left: 30.0px;">The HDF5 Python APIs use methods associated with specific objects.</p><p> </p><ul><li>For portability, the HDF5 library has its own defined types.  Some common types that you will see in the example code are:</li></ul><p style="margin-left: 90.0px;"> <code>hid_t</code> is used for object handles</p><p>                        <code>hsize_t</code> is used for dimensions</p><p>                        <code>herr_t</code><strong> </strong>is used for many return values</p><p> </p><ul><li>Language specific files must be included in applications:</li></ul><p style="margin-left: 90.0px;">Python:<strong>            </strong>Add “<code>import h5py</code>” / “<code>import numpy</code>”</p><p style="margin-left: 90.0px;">C:                     Add “<code>#include hdf5.h</code>”</p><p style="margin-left: 90.0px;">FORTRAN:       Add “<code>USE HDF5</code>&quot; and call <code>h5open_f</code> and <code>h5close_f</code> to initialize and close the HDF5 FORTRAN  interface</p><p> </p><h3 id="IntroductiontoHDF5-Stepstocreateafile:">Steps to create a file:</h3><p>To create an HDF5 file you must:</p><ol><li>Specify property lists (or use the defaults).</li><li>Create the file.</li><li>Close the file (and property lists if needed).</li></ol><p>Example:</p><p>The following Python and C examples create a file, <code>file.h5</code>, and then close it. The resulting HDF5 file will only contain a <em>root</em> group:</p><p style="margin-left: 30.0px;"><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image confluence-thumbnail" width="200" src="/download/thumbnails/50078525/crtf-pic.png?version=1&amp;modificationDate=1517605912479&amp;api=v2" data-image-src="/download/attachments/50078525/crtf-pic.png?version=1&amp;modificationDate=1517605912479&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078820" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="crtf-pic.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p> </p><p><u>Python:</u></p><p>Calling h5py.File with ‘w’ for the file access flag will create a new HDF5 file and overwrite an existing file with the same name.  “file” is the file handle returned from opening the file.  When finished with the file, it must be closed. When not specifying property lists, the default property lists are used:</p><p style="margin-left: 60.0px;"><code>import h5py</code></p><p style="margin-left: 60.0px;"><code>file = h5py.File (‘file.h5’<strong>, ‘</strong>w’)</code></p><p style="margin-left: 60.0px;"><code>file.close ()</code></p><p><u>C:</u></p><p>The H5Fcreate function creates an HDF5 file.   H5F_ACC_TRUNC is the file access flag to create a new file and overwrite an existing file with the same name, and H5P_DEFAULT is the value specified to use a default property list.</p><p style="margin-left: 60.0px;"><code>#include “hdf5.h”</code></p><p style="margin-left: 60.0px;"><code>int main() {</code></p><p style="margin-left: 60.0px;"><code>    hid_t       file_id;</code></p><p style="margin-left: 60.0px;"><code>    herr_t      status;</code></p><p> </p><p style="margin-left: 60.0px;"><code>    file_id = H5Fcreate (&quot;file.h5&quot;, H5F_ACC_TRUNC, H5P_DEFAULT, H5P_DEFAULT);   </code></p><p style="margin-left: 60.0px;"><code>    status = H5Fclose (file_id);</code></p><p style="margin-left: 60.0px;"><code>}</code></p><h3 id="IntroductiontoHDF5-Stepstocreateadataset:">Steps to create a dataset:</h3><p>As described previously, an HDF5 dataset consists of the raw data, as well as the metadata that describes the data (datatype, spatial information, and properties). To create a dataset you must:</p><ol><li>Define the dataset characteristics (datatype, dataspace, properties).</li><li>Decide which group to attach the dataset to.</li><li>Create the dataset.</li><li>Close the dataset handle from step 3.</li></ol><p>Example:</p><p>The code excerpts below show the calls that need to be made to create a 4 x 6 integer dataset <code>dset</code> in a file <code>dset.h5</code>. The dataset will be located in the <em>root</em> group:</p><p>            <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image confluence-thumbnail" width="200" src="/download/thumbnails/50078525/crtdset.png?version=1&amp;modificationDate=1517605972625&amp;api=v2" data-image-src="/download/attachments/50078525/crtdset.png?version=1&amp;modificationDate=1517605972625&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078823" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="crtdset.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span>  </p><p><u>Python:</u></p><p>With Python, the creation of the dataspace is included as a parameter in the dataset creation method.  Just one call will create a 4 x 6 integer dataset <code>dset</code>. A pre-defined Big Endian 32-bit integer datatype is specified. The create_dataset method creates the dataset in the root group (the file object).  The dataset is close by the Python interface.</p><p style="margin-left: 60.0px;"><code> dataset = file.create_dataset(&quot;dset&quot;,(4, 6), h5py.h5t.STD_I32BE)</code></p><p><u>C:</u></p><p>To create the same dataset in C, you must specify the dataspace with the H5Screate_simple function, create the dataset by calling H5Dcreate, and then close the dataspace and dataset with calls to H5Dclose and H5Sclose. H5P_DEFAULT is specified to use a default property list. Note that the file identifier (file_id) is passed in as the first parameter to H5Dcreate, which creates the dataset in the root group.</p><p style="margin-left: 60.0px;">   <code>/* Create the dataspace for the dataset. */</code></p><p style="margin-left: 60.0px;"><code>   dims[0] = 4;</code></p><p style="margin-left: 60.0px;"><code>   dims[1] = 6;</code></p><p style="margin-left: 60.0px;"><code>   dataspace_id = H5Screate_simple(2, dims, NULL);</code></p><p style="margin-left: 60.0px;"> </p><p style="margin-left: 60.0px;"><code><strong>   </strong>/* Create the dataset. */</code></p><p style="margin-left: 60.0px;"><code>   dataset_id = H5Dcreate (file_id, &quot;/dset&quot;, H5T_STD_I32BE, dataspace_id, H5P_DEFAULT, H5P_DEFAULT, H5P_DEFAULT);</code></p><p> </p><p style="margin-left: 60.0px;"><code>   /* Close the dataset and dataspace */</code></p><p style="margin-left: 60.0px;"><code>   status = H5Dclose(dataset_id);</code></p><p style="margin-left: 60.0px;"><code>   status = H5Sclose(dataspace_id);</code></p><p>  </p><h3 id="IntroductiontoHDF5-Writingtoorreadingfromadataset:">Writing to or reading from a dataset:</h3><p>Once you have created or opened a dataset you can write to it:</p><p><u>Python:</u></p><p style="margin-left: 60.0px;"><code>data = np.zeros((4,6))</code></p><p style="margin-left: 60.0px;"><code>for i in range(4):</code></p><p style="margin-left: 60.0px;"><code>  for j in range(6):</code></p><p style="margin-left: 60.0px;"><code>     data[i][j]= i*6+j+1</code></p><p style="margin-left: 60.0px;"> <code>dataset[...] = data  </code>         <strong>&lt;-- Write data to dataset</strong></p><p style="margin-left: 60.0px;"><code>data_read = dataset[...]  </code><strong>&lt;-- Read data from dataset</strong></p><p><u>C:</u></p><p>H5S_ALL is passed in for the memory and file dataspace parameters to indicate that the entire dataspace of the dataset is specified. These two parameters can be modified to allow subsetting of a dataset. The native predefined datatype, H5T_NATIVE_INT, is used for reading and writing so that HDF5 will do any necessary integer conversions:</p><p style="margin-left: 60.0px;"><code>status = H5Dwrite (dataset_id, H5T_NATIVE_INT, H5S_ALL, H5S_ALL, H5P_DEFAULT, dset_data);</code></p><p style="margin-left: 60.0px;"><code>status = H5Dread (dataset_id, H5T_NATIVE_INT, H5S_ALL, H5S_ALL,   H5P_DEFAULT, dset_data);</code></p><p> </p><h3 id="IntroductiontoHDF5-Stepstocreateagroup:">Steps to create a group:</h3><p>An HDF5 group is a structure containing zero or more HDF5 objects. Before you can create a group you must obtain the location identifier of where the group is to be created. Following are the steps that are required:</p><ol><li>Decide where to put the group – in the “root group” (or file identifier) or in another group. Open the group if it is not already open.</li><li>Define properties or use the default.</li><li>Create the group.</li><li>Close the group.</li></ol><p>Example:</p><p><br/> This example illustrates how to create a group MyGroup that is attached to the root group. If the file identifier is specified for the location of the group it will be created in the root group.</p><p style="margin-left: 30.0px;"><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image confluence-thumbnail" width="300" src="/download/thumbnails/50078525/crtgrp.png?version=1&amp;modificationDate=1517605933930&amp;api=v2" data-image-src="/download/attachments/50078525/crtgrp.png?version=1&amp;modificationDate=1517605933930&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078821" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="crtgrp.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span></p><p><u>Python:</u></p><p>The code below opens the dataset dset.h5 with read/write permission and creates a group MyGroup in the root group. Properties are not specified so the defaults are used:</p><p style="margin-left: 60.0px;"><code>import h5py</code></p><p style="margin-left: 60.0px;"><code>file = h5py.File('dset.h5', 'r+')  </code></p><p style="margin-left: 60.0px;"><code>group = file.create_group ('MyGroup')</code></p><p style="margin-left: 60.0px;"><code>file.close()</code></p><p style="margin-left: 60.0px;"> </p><p><u>C:</u></p><p>To create the group MyGroup in the root group, you must call H5Gcreate, passing in the file identifier returned from opening or creating the file. The default property lists are specified with H5P_DEFAULT. The group is then closed:<u><br/> <br/> </u></p><p style="margin-left: 60.0px;"><code>group_id = H5Gcreate (file_id, &quot;MyGroup&quot;, H5P_DEFAULT, H5P_DEFAULT, H5P_DEFAULT);</code></p><p style="margin-left: 60.0px;"><code>status = H5Gclose (group_id);</code></p><p><strong> </strong></p><h3 id="IntroductiontoHDF5-Stepstocreateandwritetoanattribute:">Steps to create and write to an attribute:</h3><p>To create an attribute you must open the object that you wish to attach the attribute to. Then you can create, access, and close the attribute as needed:</p><ol><li>Open the object that you wish to add an attribute to.</li><li>Create the attribute</li><li>Write to the attribute</li><li>Close the attribute and the object it is attached to.</li></ol><p>The example below creates attributes that are attached to the dataset <code>dset</code>:<br/><br/><span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" width="315" src="/download/attachments/50078525/crtatt.png?version=1&amp;modificationDate=1517605958837&amp;api=v2" data-image-src="/download/attachments/50078525/crtatt.png?version=1&amp;modificationDate=1517605958837&amp;api=v2" data-unresolved-comment-count="0" data-linked-resource-id="50078822" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="crtatt.png" data-base-url="https://confluence.hdfgroup.org" data-linked-resource-content-type="image/png" data-linked-resource-container-id="50078525" data-linked-resource-container-version="57"></span>      </p><p><u>Python:</u></p><p>The dataspace, datatype, and data are specified in the call to create an attribute in Python:</p><p style="margin-left: 30.0px;"><code>dataset.attrs[&quot;Units&quot;] = “Meters per second”</code>  <strong>&lt;-- Create string</strong></p><p style="margin-left: 30.0px;"><code>attr_data = np.zeros((2,))</code></p><p style="margin-left: 30.0px;"><code>attr_data[0] = 100</code></p><p style="margin-left: 30.0px;"><code>attr_data[1] = 200</code></p><p style="margin-left: 30.0px;"><code>dataset.attrs.create(&quot;Speed&quot;, attr_data, (2,), “i”)</code> <strong>&lt;-- Create Integer</strong></p><p><u>C:</u></p><p>To create an integer attribute in C, you must create the dataspace, create the attribute, write to it and then close it in separate steps:</p><p style="margin-left: 30.0px;"><code>/* Create the data space for the attribute. */

</code></p><p style="margin-left: 30.0px;"><code>dims = 2;

</code></p><p style="margin-left: 30.0px;"><code>dataspace_id = H5Screate_simple(1, &amp;dims, NULL);


</code></p><p style="margin-left: 30.0px;"><code>/* Create a dataset attribute. */

</code></p><p style="margin-left: 30.0px;"><code>attribute_id = H5Acreate2 (dataset_id, &quot;Units&quot;, H5T_STD_I32BE, dataspace_id, H5P_DEFAULT, H5P_DEFAULT);


</code></p><p style="margin-left: 30.0px;"><code>/* Write the attribute data. */

</code></p><p style="margin-left: 30.0px;"><code>status = H5Awrite(attribute_id, H5T_NATIVE_INT, attr_data);


</code></p><p style="margin-left: 30.0px;"><code>/* Close the attribute. */

</code></p><p style="margin-left: 30.0px;"><code>status = H5Aclose(attribute_id);</code></p><p> </p><p> </p><p> </p>

                
        
    
		<div class="clear block-toggle"></div></div><!-- /.content-block --><div class="brikit-content-block original designable-element  from-layout   position-bottom     hdf-last-modified-block" id="content-block-945700901" data-content-block="945700901"  style="
																	"><p>--- Last Modified: February 08, 2018 | 08:54 AM</p><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column --></div></div></div></div></div><!-- /.brikit-content-layer-container --><div class=" brikit-container-backdrop brikit-content-layer-backdrop brikit-content-layer   from-layout   hdf-footer-shim" id="content-layer-1310479910" data-content-layer="1310479910" data-name=""
	style="		 height:false; 							background-color:#151515;
													"
	><div class=" brikit-container brikit-content-layer-container "
			><div class=" brikit-container-content brikit-layer " style="		 height:false; 																										"
			><div class="brikit-content-layer-table"
				><div class="brikit-content-layer-table-row designable-element"><p>
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-1310479911" data-content-column="1310479911"
	style="
		 width:100%; 	 height:false; 											">
		<div class="column-wrapper">
					<p> </p>
		</div>
	</div>
<!-- /.content-column --></p></div></div></div></div></div><!-- /.brikit-content-layer-container --><style id="content-layout-styles">

	.brikit-container { 			width: 100%;
		margin: 0;
	 }
	.tp-content-container { max-width: $container-width; }

					</style>
	
			
	
</div>

        <!--
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:dc="http://purl.org/dc/elements/1.1/"
         xmlns:trackback="http://madskills.com/public/xml/rss/module/trackback/">
         <rdf:Description
    rdf:about="https://confluence.hdfgroup.org/display/HDF5/Introduction+to+HDF5"
    dc:identifier="https://confluence.hdfgroup.org/display/HDF5/Introduction+to+HDF5"
    dc:title="Introduction to HDF5"
    trackback:ping="https://confluence.hdfgroup.org/rpc/trackback/50078525"/>
</rdf:RDF>
-->

					        
			
					
					        
    		
            
</div>

	    

    




    
    

    
    
    


    
<div id="space-tools-web-items" class="hidden">
                <div data-label="Overview" data-href="/spaces/viewspacesummary.action?key=HDF5">Overview</div>
            <div data-label="Content Tools" data-href="/pages/reorderpages.action?key=HDF5">Content Tools</div>
            <div data-label="Add-ons" data-href="/zen/space/viewzenconfigure.action?key=HDF5">Add-ons</div>
            <div data-label="Activity" data-href="/spaces/usage/report.action?key=HDF5">Activity</div>
            <div data-label="Tasks" data-href="/spaces/tasksreport.action?key=HDF5">Tasks</div>
    </div>


        



																			</div><!-- .brikit-content-stack -->
					
					<div id="brikit-footer-shim"></div>
						<div class="brikit-container-backdrop brikit-footer-backdrop " >
		<div class="brikit-container brikit-footer-container">
	    	<div  class="brikit-container-content brikit-footer">
												<div  id="brikit-footer" 				 class="brikit-footer-content "
				 data-page-id="48802346">
				<div class=" brikit-architect-page-container    " id="content-layer-1" data-content-layer="1" data-name=""
	style="		 height:false; 																	"
	><div class=" brikit-architect-table "
			><div class=" brikit-architect-container-content " style="		 height:false; 																										"
			><div class="brikit-content-layer-table"
				><div class="brikit-content-layer-table-row designable-element"><p><script type="text/javascript" src="https://jira.hdfgroup.org/s/50442344ad45b552b9ccd4add847870e-T/en_US-zcxv0v/71008/8d5b4d80dd130c97be4ba5d5af6a991b/2.0.11/_/download/batch/com.atlassian.jira.collector.plugin.jira-issue-collector-plugin:issuecollector/com.atlassian.jira.collector.plugin.jira-issue-collector-plugin:issuecollector.js?locale=en-US&collectorId=a2a1ffe0"></script></p>
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-11" data-content-column="11"
	style="
		 width:36.363636%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-111" data-content-block="111"  style="
																	"><h5 style="text-align: left;" id="id-.brikit.footer.HDF-TheHDFGroup">The HDF Group</h5><p style="text-align: left;">Copyright © 2006-2018<br/>All rights reserved</p><p style="text-align: left;">HDF is a registered trademark of The HDF Group.</p><p style="text-align: left;"><a class="external-link" href="https://www.hdfgroup.org/privacy-policy/" rel="nofollow">Privacy Policy</a> | <a class="external-link" href="https://www.hdfgroup.org/terms-of-service/" rel="nofollow">Terms of Service</a></p><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column -->
	<div class="brikit-content-column brikit-content-column-alternate designable-element
						" id="content-column-12" data-content-column="12"
	style="
		 width:21.212122%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-121" data-content-block="121"  style="
																	"><h5 id="id-.brikit.footer.HDF-Site">Site</h5><ul><li><a href="/display/support/HDF+Support+Portal">Home</a></li><li><p><a href="/display/support/Site+Map">Site Map</a></p><p> </p></li></ul><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column -->
	<div class="brikit-content-column brikit-content-column-normal designable-element
						" id="content-column-13" data-content-column="13"
	style="
		 width:21.212122%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-131" data-content-block="131"  style="
																	"><h5 id="id-.brikit.footer.HDF-Resources">Resources</h5><ul><li><a href="/display/knowledge">Knowledge Base</a></li><li><a href="/display/support/The+HDF+Help+Desk">Help Desk</a></li><li><a href="/display/support/Downloads">Downloads</a></li></ul><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column -->
	<div class="brikit-content-column brikit-content-column-alternate designable-element
						" id="content-column-15" data-content-column="15"
	style="
		 width:21.212122%; 	 height:false; 											">
		<div class="column-wrapper">
					<div class="brikit-content-block original designable-element      " id="content-block-151" data-content-block="151"  style="
																	"><h5 id="id-.brikit.footer.HDF-Connect">Connect</h5><ul><li><a class="external-link" href="https://www.hdfgroup.org" rel="nofollow">Main Website</a></li><li><a class="external-link" href="https://twitter.com/hdf5" rel="nofollow">Twitter</a></li><li><a class="external-link" href="https://www.hdfgroup.org/blog/" rel="nofollow">Blog</a></li></ul><div class="clear block-toggle"></div></div><!-- /.content-block -->
		</div>
	</div>
<!-- /.content-column --></div></div></div></div></div><!-- /.brikit-content-layer-container -->

								<div style="clear:both"></div>
			</div>
											</div>
		</div>
	</div>


					<style type="text/css">

	body {
		 background-color: #F5F5F5;
	}

	.presentation-mode #header,
	#header.hide {
		position: absolute;
	}

	#header.fixed-header {
		position: relative !important;
	}

	.presentation-mode .ia-fixed-sidebar,
	.ia-fixed-sidebar.hide {
		display: none;
	}

	.presentation-mode .brikit-toolbar,
	.presentation-mode #brikit-simple-toolbar-toggle,
	.presentation-mode #header-precursor,
	.brikit-toolbar.hide {
		display: none;
	}

	
	.presentation-mode .brikit-header-backdrop,
	.presentation-mode .brikit-footer-backdrop,
	.presentation-mode .brikit-toolbar,
	.presentation-mode .drag-handle,
	.presentation-mode .edit-content-block {
		display: none !important;
	}

	.presentation-mode .presentation-notes {
		display: none;
	}
	
	.presentation-mode .brikit-title-backdrop {
		margin-top: 0;
	}
	
	.hide-mouse,
	.hide-mouse * {
		cursor: none;
	}
	
	.frames .drag-handle {
		display: none !important;
	}
	
	.brikit-content-block .block-back,
	.brikit-content-block .rotator-help {
		display: none;
	}

</style>
		
					<script type="text/javascript">
		(function ($) {

		// PRESS-1388: Table of Contents macro displays superfluous or irrelevant results
		$(".client-side-toc-macro").removeClass("client-side-toc-macro").addClass("client-side-toc-macro-patch");
		
		// Prune out any restricted content, and the resulting empty containers it leaves behind
		// (PRESS-1150: Restrict Content macro leaves empty whitespace when content is hidden)
		$(".restricted-content").each(function () {
			var $remove = $(this);
			// PRESS-1600: If the restriction specifies another element, replace the restrict content with that element
			if ($remove.hasAttr("data-selector")) {
				var $consolation = $($remove.data("selector"));
				$remove.replaceWith($consolation.show());
			}
			else {
				while ($remove.length) {
					var $parent = $remove.parent();
					$remove.remove();
					$remove = jQuery.trim($parent.html()).length ? "" : $parent;
				}
			}
		});

		// Make sure the mobile phone page title suffix doesn't display to mobile users
		if (themePressMobile) {
			var text = $("\#title-text a").text();
			var index = text.indexOf(".mobile.phone");
			if (index != -1) $("\#title-text a").text(text.substring(0, index));
		}
		
		// Hide the header, toolbar, sidebar initially to suppress the flash
		$("#header, .brikit-toolbar.normal, .ia-fixed-sidebar").addClass("hide");
		
		// If the toolbar is empty, just get rid of it
		if (!jQuery.trim($(".brikit-toolbar").html()).length) $(".brikit-toolbar").remove();
		
		// PRESS-988: Force the header to be full width on load
		$("#header").width($("#main").outerWidth(true));
		
		// Zap any IDs from content-column and content-block macros rendered inside headers, footers, and menus to avoid
		// conflicts with content on the current page
		$(".brikit-content-column, .brikit-content-block", ".brikit-architect-container-content").removeAttr("id");

	if (!$("#main-content.frames").length) {
		// Ensure each layer has a main column (the page is not always rendered under Theme Press control)
		$("#main-content .brikit-content-layer").each(function () {
			var $mainColumn = $(".brikit-content-column-main", this).first();
			if (!$mainColumn.length) {
				var widestWidth = 0;
				$(".brikit-content-column", this).each(function () {
					if ($(this).width() > widestWidth) {
						widestWidth = $(this).width();
						$mainColumn = $(this);
					}
				});
				$mainColumn.addClass("brikit-content-column-main");
			}
		});
		
		// In a mobile context, in each layer, move all non-main columns below the main column
		if (themePressMobile) {
			$("#main-content .brikit-content-layer").each(function () {
				var $mainColumn = $(".brikit-content-column-main", this).first();
				var $before = $mainColumn.prevAll().not(".mobile-hide").show();
				var $after  = $mainColumn.nextAll().not(".mobile-hide").show();
				$mainColumn.after($before).after($after);
			});
		}
		else if (contentContainerWidth > 0) {
			// Handle browser windows narrower than the content container + .brikit-toolbar padding-right
			$("#main").css("min-width", contentContainerWidth + 24);

			// Add a fake stripe to visually extend the header/toolbar
			var $stripe = $("<div>").attr("id", "header-fake-stripe").append($("<div>").addClass("bottom-stripe"));
			$("#brikit-load-overlay").before($stripe);
		}
	}
		
							if (!themePressMobile) ThemePress.relocateElement("#quick-search", "#brikit-search");
				
						
				// Zap the page metadata if not wanted (it displays through the standard Confluence mechanism regardless, so this step is needed)
					$("#page-metadata-hide .page-metadata").hide();
				
		// If breadcrumbs should be relocated, move it
				if (themePressMobile) $("#breadcrumb-section").remove();
		else $("#breadcrumb-section").show();
		
		// If metadata banner should be hidden or moved, do it
					$("#page-metadata-banner").hide();
		
		// Move the title if it is transient (marked for moving to main column)
		var $transientTitle = $("#brikit-main-column-title");
		if (!$(".brikit-breadcrumbs, .brikit-page-title, .brikit-page-metadata", $transientTitle).isHidden(true)) {
			$(".brikit-content-layers .brikit-content-column-main").first().prepend($transientTitle.addClass("brikit-content-block from-layout main-column-addition").show());
		}
		$("\#title-heading").show();
		
		// Move the labels if marked to move to the main column
		var $lastMainColumn = $(".brikit-content-layers .brikit-content-column-main").last();
				if (themePressMobile) $(".brikit-labels-backdrop").remove();
		
		// Move the comments if marked to move to the main column
					
		// Clean up page meta data in mobile view
		if (themePressMobile) {
			var mobilizeMetadata = function () {
				$(".page-metadata").each( function () {
					$(".author a, .editor a", this).unbind();
					$(".last-modified", this).attr("href", "#").attr("onclick", "return false;");
				});
			};

			var mobilizeProfileMacro = function () {
				$(".confluence-userlink, .userLogoLink", this).unbind();
			};

			mobilizeMetadata();
			mobilizeProfileMacro();
			
			$(document).ajaxComplete(mobilizeMetadata).ajaxComplete(mobilizeProfileMacro);
			
		}
		
		// Clean up comments in mobile view
		if (themePressMobile) $(".brikit-comments-backdrop").remove();

		// Set up any tabbed block areas
		if (!themePressMobile) $(".tabbed-blocks").each(function () {
			var column = $(this);
			var blocks = column.find(".brikit-content-block").not(".not-tabbed");
			if (!$("#main-content.frames").length) blocks = blocks.not(".from-layout");
			if (!blocks.length) return;
			
			var tabContainerId = "tab-" + column.attr("id");
			var tabs = $("<ul>").addClass("tabs-menu theme-press");
			var tabContainer = $("<div>").addClass("aui-tabs horizontal-tabs theme-press").attr("id", tabContainerId).append(tabs);
			blocks.first().before(tabContainer);
			blocks.each(function () {
				var block = $(this).addClass("tabs-pane theme-press");
				var tabId = block.attr("id");
				var tabName = block.data("name") || "Tab " + ($("li", tabs).length + 1);
				var link = $("<a>").attr("href", "#" + tabId).text(tabName);
				var tab = $("<li>").addClass("menu-item theme-press").append(link);
				tabs.append(tab);
				tabContainer.append(block);
			});
			$(".menu-item", tabs).first().addClass("active-tab");
			$(".tabs-pane", tabContainer).first().addClass("active-pane");
		});
		
		// Set up any tabbed block areas that want to be expanding blocks instead of tabs
		if (!themePressMobile) $(".expanding-block-tabs").each(function () {
			var column = $(this);
			var blocks = column.find(".brikit-content-block").not(".not-tabbed");
			if (!$("#main-content.frames").length) blocks = blocks.not(".from-layout");
			if (!blocks.length) return;

			var tabContainerId = "tab-" + column.attr("id");
			var tabContainer = $("<div>").addClass("expanding-block-tabs-container").attr("id", tabContainerId);
			blocks.hide().first().before(tabContainer);
			var count = 1;
			blocks.each(function () {
				var block = $(this).addClass("tabs-pane theme-press");
				var tabId = block.attr("id");
				var tabName = block.data("name") || "Tab " + count++;
				var link = $("<a>").attr("href", "#" + tabId).text(tabName);
				var tab = $("<div>").addClass("expanding-block-tab-trigger").append(link);
				tabContainer.append(tab);
				tabContainer.append(block);
			});
		});
		$(".brikit-canvas").on("click", ".expanding-block-tab-trigger a", function (event) {
			event.preventDefault();
			$($(this).attr("href") + " .block-toggle").click();
		});
		
		// Make sure all "new window" links open in a new window, and by default, all external links open a new window
	    $(".target-new-window a").attr("target", "_blank");
	    $(".target-current-window a").removeAttr("target");
		
		// Add a class to identify the first and last layers on the page
		$(".brikit-content-layers .brikit-content-layer").first().addClass("first-layer");
		$(".brikit-content-layers .brikit-content-layer").last().addClass("last-layer");

					
		// For mobile screens, scale any blocks flagged with or inside a "scale-mobile" class
		// Note: only works for fixed height blocks
		
	})(jQuery);
</script>
		
																			</div><!-- \#main -->
																																																																																
								    
				
				
				
				        
            
            

<div id="footer" role="contentinfo">
    <section class="footer-body">

                                                            <p class="license license-opensource">
                    Powered by a free <b>Atlassian Confluence Open Source Project License</b> granted to HDF. <a href="http://www.atlassian.com/c/conf/11461">Evaluate Confluence today</a>.<br>
                </p>
                    
        

        <ul id="poweredby">
            <li class="noprint">Powered by <a href="http://www.atlassian.com/software/confluence" class="hover-footer-link">Atlassian Confluence</a> <span id='footer-build-information'>5.9.5</span>, <a href="http://www.atlassian.com/software/confluence/overview/team-collaboration-software?utm_source=confluence-footer" class="hover-footer-link">Team Collaboration Software</a></li>
            <li class="print-only">Printed by Atlassian Confluence 5.9.5, Team Collaboration Software.</li>
            <li class="noprint"><a href="https://jira.atlassian.com/browse/CONF" class="hover-footer-link">Report a bug</a></li>
            <li class="noprint"><a href="http://www.atlassian.com/about/connected.jsp?s_kwcid=Confluence-stayintouch" class="hover-footer-link">Atlassian News</a></li>
        </ul>

        

        <div id="footer-logo"><a href="http://www.atlassian.com/">Atlassian</a></div>

                    
        
    </section>
</div>

    
			</div><!-- .ia-splitter -->
	
</div><!-- \#full-height-container -->
</div><!-- \#page -->
    <span style="display:none;" id="confluence-server-performance">{"serverDuration": 270, "requestCorrelationId": "91d36266fd5798"}</span>


<script type="text/javascript">
		AJS.BigPipe = AJS.BigPipe || {};
		AJS.BigPipe.metrics = AJS.BigPipe.metrics || {};
		AJS.BigPipe.metrics.pageEnd = typeof window.performance !== "undefined" && typeof window.performance.now === "function"
										? Math.ceil(window.performance.now()) : 0;
		AJS.BigPipe.metrics.isBigPipeEnabled = 'false' === 'true';
	</script>
<style>
	#brikit-load-overlay {
		display: none;
	}
</style>
</body>
<script>
window.WRM=window.WRM||{};window.WRM._unparsedData=window.WRM._unparsedData||{};
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:atlassian-nps-plugin-resources.is-server-instance-data-provider"]="true";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:browser-metrics.feature-data-provider-legacy"]="true";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-license-banner:confluence-license-banner-resources.license-details"]="{\"daysBeforeLicenseExpiry\":0,\"daysBeforeMaintenanceExpiry\":0,\"showLicenseExpiryBanner\":false,\"showMaintenanceExpiryBanner\":false,\"renewUrl\":null,\"salesEmail\":null}";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-hipchat-integration-plugin:discovery-javascript-data.link-active"]="{\"linkActive\":false,\"conditionsMet\":true,\"admin\":false}";
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:nps-acknowledgement-resources.analytics-enabled-data-provider"]="\"false\"";
WRM._unparsedData["com.atlassian.plugins.atlassian-nps-plugin:nps-acknowledgement-resources.sen-data-provider"]="\"SEN-2026567\"";
WRM._unparsedData["com.onresolve.confluence.groovy.groovyrunner:web-item-response-renderer.web-item-actions-data-provider"]="[]";
WRM._unparsedData["com.atlassian.confluence.plugins.confluence-feature-discovery-plugin:confluence-feature-discovery-plugin-resources.test-mode"]="false";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:api.feature-data-provider"]="true";
WRM._unparsedData["com.atlassian.plugins.browser.metrics.browser-metrics-plugin:api.rack-data-provider"]="\"\"";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-context"]="{\"hostApplication\":{\"id\":\"0a60c7cc-4441-329b-a406-db7975d29eab\",\"type\":\"confluence\"}}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-features"]="{\"BITBUCKET_REBRAND\":true,\"V3_UI_OPT_IN\":false,\"V3_UI\":false}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-common.applinks-discovered-features"]="[]";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-context"]="{\"hostApplication\":{\"id\":\"0a60c7cc-4441-329b-a406-db7975d29eab\",\"type\":\"confluence\"}}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-features"]="{\"BITBUCKET_REBRAND\":true,\"V3_UI_OPT_IN\":false,\"V3_UI\":false}";
WRM._unparsedData["com.atlassian.applinks.applinks-plugin:applinks-util-js.applinks-discovered-features"]="[]";
</script>





</html>
    
