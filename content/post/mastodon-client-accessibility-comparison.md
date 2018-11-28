---
title: "Mastodon Client Accessibility Comparison"
date: 2018-11-28 16:55:46 
author: "Ryan Ricard"
description: "Mastodon Client Accessibility Comparison"
draft: true
---

Can write CWs
Shows CWs
CW Show/Hide interaction
Can write image descriptions
Can read image descriptions
Can write video/gif descriptions
Can read video/gif descriptions
VoiceOver support
Respect's system font choice
Color theme options
Respects "Reduce Motion"


Feature                          | Amaroq         | Mast           | Toot!          | Tootdon        | Tootle         | Tusk           |
---------------------------------|----------------|----------------|----------------|----------------|----------------|----------------|         
12345678123456781234567812345678 |1234567812345678|1234567812345678|1234567812345678|1234567812345678|1234567812345678|1234567812345678|
Can View Content Warnings        | Yes            | Yes (Config)   | Yes            | Yes            | Yes            | Yes (Config)   |
Can Write Content Warnings       | Yes            | Yes            | Yes            | Yes            | Yes            | No             |
CW Show/Hide with                | Long Press     | Tap            | Tap            | Tap            | Tap            | Tap            |
Can Write Image Descriptions     | Yes            | Yes            | Yes            | No             | No             | No             |
Can Read Image Descriptions      | V/O Only       | No             | Yes            | No             | Yes            | No             |
Can Write Video Descriptions     | Yes            | Yes            | N/A            | No             | No             | No             |
Can Read Video Descriptions      | No             | No             | No             | No             | No             | No             |
Color Theme Options              | 1              | 4              | 1              | 2              | 5              | 1              |
Can Control Gif Animation        | Yes            | Hide Images    | No             | Yes            | Yes            | N/A            |
VoiceOver Support                | Yes            | No[1]          | No[2]          | No[1]          | No [3]         | No [1]         |
Respect System Font Size         | Yes            | No             | No             | No             | No             | No             |
Supports "Smart Invert"          | No             | No             | No             | No             | No             | No             |

## Description of Features Tested

### Content Warnings

Content Warnings are a way for a poster to give a description of a post and suggest that it be hidden behind an action in a client UI (requiring e.g. a button tap to open the full post's contents). Content warnings make Mastodon a more pleasant experience for people with many different disabilities, including post-traumatic stress disorder, autism spectrum disorder, and epilepsy. Many readers without those disabilities also find that CWs give them more control over their reading experience, allowing them to avoid subjects that are unpleasant or uninteresting to them. Many Mastodon instances have developed strong norms around putting Content Warnings on certain categories of posts. 

### Image and Video Descriptions

Adding written descriptions of images and videos makes posts with images more accessible to blind and low-vision readers. In the Mastodon web UI, image descriptions are rendered as both the `alt` attribute, intended for screen readers or situations where images cannot be displayed, and the `title` attribute, which is visible in desktop browsers on mouse-over. This is a good example of designing [accessibility for everyone](https://abookapart.com/products/accessibility-for-everyone), as both people with disabilities and the nondisabled can use and benefit from the feature. Many Mastodon instances 


1: Voiceover won't read image descriptions
2: Image descriptions work, but usernames are never read with toots.
3: Image descriptions work, but I can't get VoiceOver to read entire toots