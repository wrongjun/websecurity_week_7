# Project 7 - WordPress Pentesting

Time spent: 6 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) 3.9.3-4.2 Stored XSS
  - [ ] Summary: XSS on comment limited. When comment is oversize, the database will truncated the comment with auto embraced.
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: 
        1) comment in a post with 64KB length of comment
        
<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>
          
  - [ ] Steps to recreate: <img src="my_gif_walkthrough_url" width="800">
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="my_gif_walkthrough_url" width="800">
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: XSS vlunerabilities existes in the playlist functionality of wordpress. vlunerabbilities can be exploites
  by malicious media file via editor or administrator.
    - Vulnerability types: XSS
    - Tested in version:4.2
    - Fixed in version: 4.7.2
  - [ ] GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week_7/blob/master/xss_attack_media.gif" width="800">
  - [ ] Steps to recreate: 
      https://www.securify.nl/advisory/SFY20160742/xss.mp3
      this mp3 is from https://seclists.org/oss-sec/2017/q1/563
      1) upload MP3 file to the Media Library (as Editor or Administrator).
      2) Insert an Audio Playlist in a Post containing this MP3 (Create Audio
          Playlist).
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [XSS via Media FIle](https://seclists.org/oss-sec/2017/q1/563)

GIFs created with [peel](https://github.com/phw/peek).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [nwrong]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
