# Content Standards

In the interest of providing accurate, up to date, and well formatted resources, I've developed the following standards that will help me guide the management of content throughout the Blue Team Labs videos, labs, and documentation.

## Version Control
All content will be managed using proper version control where possible. For scripts, documentation, and documents, this will be managed via git-scm. 

For videos, audio files, and other multi-media, file versioning will be enabled in the respective application used to create this content. Change logs and version control information will be posted on a dedicated page for each multi-media resource. These pages will be available to any user to view revisions and updates to content as time goes on.

## Corrections
As humans, it's inveitable that we will make errors. In the event and error is made, any content impacted by this error or misinformation will be promptly made private. The reasoning behind this is to minimize the impact of users receiving improper information.

Once made private, we will make the approriate corrections, annotate the change logs, and promplty restore the content. We believe this is in the best interest of everyone, as all it takes is hearing something incorrect once and you'll believe it for the rest of your life.

In the event of a widespread error that, we will promptly communicate the error and correction to all users through whatever means are best available to us.

## Content Reuse and Attribution
Often times, we may provide commands or screenshots from a vendors documentation. We think this is easiest rather than asking you to visit the site individually and follow the instructions. At times, this may cause some of our content to appear outdated. When this occurs, we will do our best to update it as soon as possible.

Additionally, attribution is a critical aspect. Whenever we use outside documentation or command lines, we'll provide a link in the footnotes for you to learn more or visit the original source. This will look something like this:

``` title="Text with footnote included"
The quick red fox [^1] jumps over the lazy[^2] dog
```

<div class="result" markdown>
The quick red fox[^1] jumps over the lazy[^2] dog
</div>

Footnotes will appear as follows:
``` title="Footnote"
[^1]: Red foxes can reach a speed of up to 30 miles per hour. https://www.animalfoodplanet.com/how-fast-do-foxes-run/
[^2]: This dog looks quite lazy, see https://www.rd.com/wp-content/uploads/2020/09/GettyImages-1159287876-scaled.jpg
```

<div class="result" markdown>

[:octicons-arrow-down-24: Jump to footnote](#fn:1)

</div>

## Image Formatting
Sometimes, we may need to post screenshots. When we post screenshots, they will often be cropped to a specific size. We will always try to center the screenshot and have it fill the center of the container, but this may not always be possible.

In the event that images are cropped rendering text unreadable, we will provide a mechanism to view the full size image and also provide a text based read out for any items which may be unreadable.

## Privacy Redactions
Some images or video may contain names, email addresses, usernames, IP addresses, MAC addresses, or other sensitive information. All of this infomration will be blocked out using a secure method to render the text unreadable and unrecoverable.


## IoC Defanging
When dealing with IoCs, we will do our best to defang URLs, links, IP addresses, domain names, etc to prevent inadvertently visiting a known malicious link. 

Defanging Examples:
=== "IPv4"
    ```
        1.1.1.1 --> 1[.]1[.]1[.]1
    ```
=== "IPv6"
    ```
        2001:4860:4860::8888 --> 2001[:]4860[:]4860[::]8888
    ```
=== "Domain Names"
    ```
        example.malicious.com --> example[.]malicious[.]com
    ```
=== "URLs"
    ```
        https://malicious.com --> hxxps[://]malicious[.]com
        ftp://malicious.com --> fxx[://]malicious[.]com
    ```
=== "Email Addreses"
    ```
        email@malcious.com --> email[@]malicious[.]com
    ```

## Malware Samples
From time to time, we may need to test the capabilities of a system by purposely injecting malware on to it. When doing so, we'll try to use tools like msfvenom and walk you along the process of creating a malicious payload yourself so you can be sure it's not doing anything you don't intend.

If we do end up sharing samples, which we don't intend to, they'll be shared in a password protected .zip file using the password _"infected"_.


## Content Quality
Quality is of the upmost important to us. While we might accept things like typos, grammatical errors, or minor punctuation errors, we won't accept low effort and low quality content. If you find our content to be of low effort or quality, please call us out and we will promptly resolve this issue.

In the effort of getting you familiar with version control, we actually suggest creating an issue on our documentations Gitlab repo :smiley:
```
This is where our instructions for creating an issue, if we had one!
```

## Things we Say or Do
We're humans, and we want to sound like humans. Rather than policing our verbiage and conforming to robotic means of communication, we'll just be ourself. This means we might say or do some things that make you scratch your head. We're okay with that. Don't worry, we'll never intentionally do anything stupid...or would we? :thinking:

## Accesibility
Where possible, we will do our best to make our content available to as diverse and audience as possible. For audio and video, this might mean text transcripts or audio transcriptions of an image or video sequence for those with visual or audio impairments. When these are available, text transcriptions will be available in the videos content captioning as well as on our documentation page.

[^1]: Red foxes can reach a speed of up to 30 miles per hour. [https://www.animalfoodplanet.com/how-fast-do-foxes-run/](https://www.animalfoodplanet.com/how-fast-do-foxes-run/)
[^2]: This dog looks quite lazy, see [https://www.rd.com/wp-content/uploads/2020/09/GettyImages-1159287876-scaled.jpg](https://www.rd.com/wp-content/uploads/2020/09/GettyImages-1159287876-scaled.jpg)
