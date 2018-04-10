# Project 7 - WordPress Pentesting

Time spent: >20 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Vulnerability Name: XSS Attack
  - [ ] Summary: XSS Attack by posting harmful code in post
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [ ] GIF Walkthrough: 
  ![alt text](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%237-WordPress%20Pentesting/week%237_1.gif)
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
2. Vulnerability Name: User Enumeration
  - [ ] Summary: User Enumeration to find a valid user
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.7.5
  - [ ] GIF Walkthrough: 
  ![alt text](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%237-WordPress%20Pentesting/week%237_2.gif)
    - [Link 2](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
3. Vulnerability Name: Malicious Filename to XSS
  - [ ] Summary: Malicious Filename to XSS
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [ ] GIF Walkthrough: 
  ![alt text](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%237-WordPress%20Pentesting/week%237_3.gif)
  - [ ] Steps to recreate: 
    - A WordPress admin uploads a malicious image file requested by a user this admin trusts or a popular malicious image that was spread via social media in the form of "attachment page". This involves social engineering. In the Proof of Concept the file name <img src=a onerror=alert(document.cookie)>.jpg was used. 
    - Whenever the attachment file is opened in its own page, xss expolited script is run.
  - [ ] Affected source code:
    - [Link 3](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)

4. Vulnerability Name: Stored XSS through embedded URL
  - [ ] Summary: Stored XSS through embedded URL
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: 
  ![alt text](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%237-WordPress%20Pentesting/week%237_4.gif)
  - [ ] Steps to recreate: 
    - make a post/page containing harmful embedded link such as: " [embed src='https://youtube.com/embed/12345\x3csvg onload=alert(12312313)\x3e'][/embed] "
  - [ ] Affected source code:
    - [Link 4](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
 
## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes
    Copyright [2018] [Shofiqur Rahman]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
