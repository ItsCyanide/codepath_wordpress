# codepath_wordpress

# Project 7 - WordPress Pen Testing

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. (Required) 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)

- [X] Summary: 
  - Vulnerability types: XSS
  - Tested in version:4.2
  - Fixed in version: 4.3.1
- [X] GIF Walkthrough: 
![rj_vulner_1](https://user-images.githubusercontent.com/59351534/200030639-2aa546b1-00dd-41f9-913e-321ce8e7bd8b.gif)
- [X] Steps to recreate: 
  - First, login as Admin
  - Next, create a new post.
  - Next, create a shortcode segment.
  - Lastly, create the post and view the page.
- [X] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/shortcodes.php?rev=54319)
  
### 2. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename

- [X] Summary: 
  - Vulnerability types: XSS
  - Tested in version: 4.2
  - Fixed in version: 4.6.10
- [X] GIF Walkthrough: 
![rj_vulner_2](https://user-images.githubusercontent.com/59351534/200031027-f2c6616e-6882-4045-9744-d91acdf3c574.gif)
- [X] Steps to recreate: 
  -  First, login as admin
  -  Next, create a new page.
  -  Once is the new page is created, add the image file name with XSS inside.
  -  Lastly, visit the new page
- [X] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/post-new.php)

### 3. (Required) WordPress 4.0-4.7.2 Authenticated Stored Cross-Site Scripiting(XSS) in Youtube URL Embeds

- [X] Summary: 
  - Vulnerability types: XSS
  - Tested in version:4.1.1
  - Fixed in version:4.1.16
- [X] GIF Walkthrough: 
![rj_vulner_3](https://user-images.githubusercontent.com/59351534/200028810-b9661987-91b2-4057-b5a5-9cbbc9457f06.gif)
- [X] Steps to recreate: 
  - First, create a post.
  - Next, edit the post as text.
  - Lastly, paste [embed src='https://www.youtube.com/embed/22222\x3csvg onload=alert(35)\x3e'][/embed]
- [X] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/shortcodes.php?rev=54319)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ...
<!-- Recommended GIF Tools:
[Kap](https://getkap.co/) for macOS
[ScreenToGif](https://www.screentogif.com/) for Windows
[peek](https://github.com/phw/peek) for Linux. -->

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
