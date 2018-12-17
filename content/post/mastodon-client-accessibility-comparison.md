---
title: "Mastodon Client Accessibility Comparison"
date: 2018-12-17 16:23:29
author: "Ryan Ricard"
description: "Mastodon Client Accessibility Comparison"
draft: true
---

<style>
	table, th, td{
		border: 1px solid rgb(169, 169, 179);
		border-collapse: collapse;
	}
	td, th{
		padding: 5px;
	}
	td.no{
		text-decoration: underline;
		text-decoration-color: #FF3640;
	}
	td.yes{
		text-decoration: underline;
		text-decoration-color: #62E864;
	}
</style>

There's been a significant growth in the number of available [Mastodon](https://joinmastodon.org/) apps for iOS in the past few months, with newcomers like Mast and Toot! joining more mature apps like Amaroq and Tootdon, resulting in quite a few choices for iPhone-having Mastodon users. I'm excited to see this diversity of choices and approaches to client apps - it reminds me of the time when Twitter still embraced 3rd-party apps and we saw a great deal of [innovation](https://daringfireball.net/2009/04/twitter_clients_playground) in what a social media app can do. 

One of the first questions I have about a new iOS Mastodon app is whether it supports common accessibility features. Mastodon has set a new high bar, both technically and culturally, for a social network that is accessible by all types of people, and I think the ecosystem of client apps should continue to push that boundary forward. Though my vision is correctible to 20-20 using a common [accessibility device](https://en.wikipedia.org/wiki/Glasses), my [home instance](https://mspsocial.net/) and the wider Fediverse both have strong norms around accessibilty for blind and low-vision users (as well as other disabilities) and I want a Mastodon app that helps me be a good citizen on the platform. 

To that end, I tested all of the popular iOS Mastodon apps for support of a number of important accessibility features. My findings are replicated in the chart below. I'm in the beta testing program for a few of these apps, so if you see a "Yes", it could mean that the feature is coming soon in a not-yet-released version. 

**Updated:** December 2018

## Feature Comparison Table

User Can...                      | [Amaroq][1]    | [Mast][2]      | [Toot!][3]     | [Tootdon][4]   | [Tootle][5]    | [Tusk][6]      |
---------------------------------|----------------|----------------|----------------|----------------|----------------|----------------|         
View Content Warnings            | Yes            | Yes (1)        | Yes            | Yes            | Yes            | Yes (1)        |
Write Content Warnings           | Yes            | Yes            | Yes            | Yes            | Yes            | No             |
Show/Hide CW with                | Long Press     | Tap            | Tap            | Tap            | Tap            | Tap            |
Write Image Descriptions         | Yes            | Yes            | Yes            | No             | No             | No             |
Read Image Descriptions          | V/O Only       | No             | Yes            | No             | Yes            | No             |
Write Video Descriptions         | Yes            | Yes            | N/A            | No             | No             | No             |
Read Video Descriptions          | No             | No             | No             | No             | No             | No             |
Color Theme Options              | 1              | 4              | 1              | 2              | 5              | 1              |
Control Gif Animation            | Yes            | Hide Images    | No             | Yes            | Yes            | N/A            |
VoiceOver Support                | Yes            | No (2)         | No&nbsp;(3)    | No (2)         | No (4)         | No (2)         |
Set System Font Size             | Yes            | No             | No             | No             | No             | No             |
Supports "Smart Invert"          | No             | No             | No             | No             | No             | No             |

[1]: https://itunes.apple.com/us/app/amaroq-for-mastodon/id1214116200?mt=8
[2]: https://itunes.apple.com/us/app/mast/id1437429129?mt=8
[3]: https://itunes.apple.com/us/app/toot/id1229021451?mt=8
[4]: https://itunes.apple.com/us/app/tootdon-for-mastodon/id1282283934?mt=8
[5]: https://itunes.apple.com/us/app/tootle-for-mastodon/id1236013466?mt=8
[6]: http://tusk.webflow.io/


### Notes

1. Whether to hide CW'd posts or not is configurable
1. Voiceover won't read image descriptions
2. Image descriptions work, but usernames are never read with toots.
3. Image descriptions work, but I can't get VoiceOver to read entire toots

## Description of Features Tested

### Content Warnings

Content Warnings are a way for a poster to give a description of a post and suggest that it be hidden behind an action in a client UI (requiring e.g. a button tap to open the full post's contents). Content warnings make Mastodon a more pleasant experience for people with many different disabilities, including post-traumatic stress disorder, autism spectrum disorder, and epilepsy. Many readers without those disabilities also find that CWs give them more control over their reading experience, allowing them to avoid subjects that are unpleasant or uninteresting to them. Many Mastodon instances have developed strong rules and norms around putting Content Warnings on certain categories of posts. 

### Image and Video Descriptions

Adding written descriptions of images and videos makes posts with images more accessible to blind and low-vision readers. In the Mastodon web UI, image descriptions are rendered as both the `alt` attribute, intended for screen readers or situations where images cannot be displayed, and the `title` attribute, which is visible in desktop browsers on mouse-over. This is a good example of designing [accessibility for everyone](https://abookapart.com/products/accessibility-for-everyone), as both people with disabilities and the nondisabled can use and benefit from the feature. Many Mastodon users encourage each other to add image descriptions to any post with images, and some Mastodon users go even further and will only boost an image-based post if it has a description. 

### Color Themes

Some low-vision users require [high contrast](http://accessibility.psu.edu/color/contrasthtml/) between the text and background color in order to read posts. People with some variation of [color blindness](https://usabilla.com/blog/how-to-design-for-color-blindness/) may also find certain color schemes easier or more difficult to use. Many users also like being able to choose between color themes to fit their aesthetic preferences. 

### Animations/Video

Auto-playing video (and animated GIFs, which for performance reasons the Mastodon web client renders as video) can be an a source of annoyance to some users, who would prefer to only play video only after a tap. This is doubly important for users with epilepsy or who are otherwise sensitive to flashing lights or repeating images. 

### VoiceOver Support

One of iOS's most important built-in accessibility features is VoiceOver, which when activated changes the function of on-screen controls to make it easier for blind and low-vision users to use a touchscreen device. When VoiceOver is activated, users can navigate an app by having the interface "read" to them by the device. For a Mastodon app to support VoiceOver correctly, users should be able to tap on a toot and hear the post read correctly. Tapping on images should also read the image description, if available. If you've never seen [VoiceOver in Action](https://www.youtube.com/watch?v=OUGOGepwsHE), I recommend checking out a demo video or [turning it on](https://www.imore.com/how-use-voiceover-iphone-and-ipad) on your own device - it's a very impressive accesibility feature. 

### Font Size

iOS lets users set a system-wide font size in the settings app that allows them to comfortably read text. Apps should support this user preference wherever possible, including the text of toots and user interface elements. 

### Smart Invert

In 2017, Apple added a [Smart Invert](https://9to5mac.com/2017/06/09/ios-11-dark-mode-smart-invert-colors-how-to-enable/) feature that can increase user interface contrast without distorting images. As of December 2018, no major Mastodon apps support this feature. 

## Conclusion




<script type="text/javascript">
	var cells = document.querySelectorAll("td");

	cells.forEach(function(c) {
	  if (c.textContent.includes("Yes")){
	  	c.classList.add("yes");
	  }
	  else if (c.textContent.includes("No")){
	  	c.classList.add("no");
	  }
	});
</script>
