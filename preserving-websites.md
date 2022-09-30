---
layout: default
title: Creating archivable websites
parent: Web Archiving
grand_parent: Services
nav_order: 1
---
# Guidance for creating archivable websites

The UK Web Archive uses the open-source Heritrix web crawler to capture the UK web domain at scale. Even though the crawler attempts to copy everything it identifies as being in scope, there is much that is beyond the current generation of web crawlers and so if your website is complex then a web crawler may not be able to read it. There are a few basic things that if taken into account when a website is designed will make a website a lot more archivable. These measures ensure preservation and help avoid information loss, if for any reason a website has to be taken offline.

## Points to consider

*The below guidance was created by [Nicola Bingham,](https://www.bl.uk/people/experts/nicola-bingham) Lead Curator for the UK Web Archive.*

1. Make sure each page of your site can be directly linked to. Modern web applications are extremely complex and often mask the underlying unique URLs that the crawler needs to discover content. It is always best practise to maintain a simple, meaningful URL structure.

2. Avoid using variable characters e.g. “?”, “=” and “&”, or unsafe characters such as the space character or the “#” character in a URL. This is because the play back software used to render archived websites sometimes has difficulty interpreting these characters. If you are using a content management system to build a website make sure that it does not generate URLs with variable or unsafe characters.

3. Use a site map to list the pages of your website which are accessible to crawlers or human users, in XML or in HTML. The sitemap should ideally be called ‘sitemap.xml' and put at the root of your web server (e.g. http://www.example.co.uk/sitemap.xml).

4. The functionality of user input forms such as search boxes will not work in the archive as the connection between the user and the hosting server is lost. If the only way to reach the content of your website is by querying a search box, the information on your website will not be available in the archived copy of the website.

5. Be aware that a web crawler can only read information on your webpage that is available when the webpage first loads. It won’t be able to read anything extra. For example, if content is loaded onto the page automatically by ‘infinite scrolling’ then the web crawler will not be access this content.

6. Archival crawlers find your content by following links, they cannot deal with URLs which are not referenced explicitly in the HTML but embedded in JavaScript or Flash presentations. If using JavaScript in your website it is a good idea to place the same content from the JavaScript in a no script tag. 

    If you use this method, ensure the contents are exactly the same as what is contained in the JavaScript, and that this content is shown to visitors who do not have JavaScript enabled in their browser. Like any functionality on the web, if it needs to contact the originating server in order to work, it will fail when archived. As a general rule of thumb, simple HTML is the easiest to archive.

7. File formats. Chose open formats or at least formats that can be read by open source software. See further guidelines on file formats in the ‘File formats’ section on page 3.

8. Video and audio files. The crawler can download some types of audio/visual files however the crucial thing is whether the crawler can discover them in the first place. If the path (URL) to the video is obfuscated, e.g. in a Javascript or Flash set up, the crawler will not be able to find them. Consider using explicit links to your video files. See further guidance on audio and video file formats on page 3.

9. Bear in mind that content hidden behind logins or sessions won’t be archived.

10. Put all your content on one website with one domain name and don’t redirect users to another
domain name. The web crawler by default reads content with a certain domain name, and if you redirect it to another domain name, then it will stop reading. For example, if your domain name is www.hlffirstworldwar.com, then don’t redirect users to [www.hlffirstworldwar.tumblr.com.](www.hlffirstworldwar.tumblr.com)

11. Be aware that embedding content into a web page using a third party service means that it is unlikely that the web crawler will be able to read it. Examples of embedding services include Flickr, Scribd, SlideShare, Storify, and SoundCloud.

12. Make sure all links work on your website, if your website contains broken links, copies of your website will also have broken links.

13. Use of robots.txt. The Standard for Robot Exclusion (SRE) is a means by which web site owners can instruct crawlers not to crawl their sites, or specify files or directories that are disallowed from a crawl, and they can even create specific rules for different crawlers. This information is contained in a file called /robots.txt which is found in the top-level directory of the web server, i.e. http://www.example.co.uk/robots.txt. 

    In order for the UKWA to successfully archive and display your website, our crawler needs to have access to all of the assets that determine how the site is rendered including images, scripts and style and layout instructions. We use the Heritrix crawler and the crawler’s User Agent identifies itself as ‘bl.uk_lddc_bot’.

14. It is good practise to conform to current web standards and [validate your code  against current web standards.](http://validator.w3.org/)

## Further reading 

* Webmaster Guidelines from Google. Many best practices mentioned here are applicable too for archiving crawlers.
http://support.google.com/webmasters/bin/answer.py?hl=en&answer=35769.

* Standford University Libraries Archivabilty (Guidelines for website owners)
https://library.stanford.edu/projects/web-archiving/archivability

* Helen Hockx-yu; Blog post on the UK Web Archive blog. How to make websites more archivable.
http://britishlibrary.typepad.co.uk/webarchive/2012/09/how-to-make-websites-more-archivable.html

* Columbia University Libraries Guidelines for Preservable websites
https://library.columbia.edu/bts/web_resources_collection/guidelines_for_preservable_websites.html