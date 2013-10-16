![Proxied Sites](https://www.evernote.com/shard/s209/sh/a6ffd5ed-9f38-4a27-9e75-1b940be94582/2f741aad7056c2bccf76844e7814773c/deep/0/Lantern.png)

The Proxied Sites screen is part of configuration for people using Lantern to Get Access, and is available through the globe icon in the lower right.

![proxy sites](https://www.evernote.com/shard/s209/sh/9dd170e2-800d-412c-bfef-8fb21819f517/22b89c58ddadf34a4dee969b2e9fe9ff/deep/0/Lantern.png)

This is where users Getting Access can set which sites to access through Lantern friends as opposed to accessing directly. By only accessing sites through Lantern that would otherwise be blocked, and accessing sites that aren't blocked directly, your experience will be faster, and Lantern will be harder to block and more efficient. The Proxied Sites screen controls what sites are routed through Lantern rather than accessed directly.

### Initial Configuration

Right now the initial list is just a number of commonly blocked sites. In the future we hope to build the list more dynamically based on what is actually blocked in each country. But for now we recommend adjusting it to your needs. If you run across a site that seems blocked, you can check if it's on the list, and add it if it's not. We also recommend removing sites from the list that are not actually blocked, as they will then load faster for you and help the network run more efficiently.

### Using a crowd-sourced proxy list

While we don't yet have a slick integration, we have set up a [Proxied Sites List Wiki](https://github.com/getlantern/lantern-proxied-sites-lists/wiki) where you can find country specific lists of blocked sites. If you live in a country with a list and it's been updated recently then it will likely work better for you than the default list that ships with lantern.

![china autoproxy list](https://www.evernote.com/shard/s209/sh/1410658e-531a-44aa-b01b-7867e074637c/b88cfe3ce617b30a394cf6c56b3ea20a/deep/0/Autoproxy%20list%20for%20china%20%C2%B7%20getlantern/lantern-proxied-sites-lists%20Wiki.png)

To make use of the a new simply go to one of the lists, then select and copy the whole list, and paste it in to your list of domains to proxy. You can do this with the mouse, selecting the list and then doing a copy on the page and a paste in your lantern. Be sure you delete your existing list (or copy over it), so you don't get duplicates and don't proxy sites you don't need to. 

![pasting in lantern.](https://www.evernote.com/shard/s209/sh/345d4873-a0b1-49e1-8188-c5356c2e5c56/d668a756c91454b8f1eaeaf79e6a79a3/deep/0/Lantern.png)

If the list is really long it can be a pain to select it all by hand. Many sites will have a link to the 'raw list', which should be a long file with just sites. If you go there you can use ctrl-a (select all), ctrl-c (copy), and ctrl-v (paste) shortcuts. You should delete the default list, so you don't get duplicates and don't proxy sites you don't need to.

### Finding Sites

Before adding a new site, you can check to see if it is already on your proxy list. This can be done by scrolling through the list, but the search box on the right lets you find it more quickly:

![searching](https://www.evernote.com/shard/s209/sh/f97bd235-eeeb-4e07-a6bd-a47f991254c1/f048f14a6d5d9aeae030ec1b00a445bb/deep/0/Lantern.png)

### Adding a new site

To add a new site, you just need to add it to a new line in the text box. You can do this anywhere you want. Just hit 'enter' to make a new line and add the site on that line.

![adding](https://www.evernote.com/shard/s209/sh/d1cf2497-2202-4929-847d-7c8c725bbdda/0028e5ba5c860863e4ca3d72014822bf/deep/0/Lantern.png)

Be sure to hit 'update' after you've entered it. Lantern will save your changes, and the next time you access that site, it will be routed through a Lantern user in your network to circumvent any blocking.

##### Formatting Note

Note that Lantern does not need or use specific parts of a site. So if you have `4.bp.blogspot.com` and `3.bp.blogspot.com` in your list you can just put `blogspot.com`. Same goes for `nobelprize.org/nobel_prizes/peace/laureates/2010`. Indeed Lantern will complain if there are `/`'s in the site, so just put the whole site: `nobelprize.org`. Search terms are similar - just put the entire search engine, and all your searches will go through Lantern. Right now there is no way to only have certain searches go through Lantern.


##### Bulk Adding of new sites

If you've got a list of proxies from another source you will likely have to clean up the formatting. Lantern does not understand any 'commenting' in its proxy list, so you will have to remove those. Make sure that you meet all the formatting requirements above. If you know [regular expressions](http://www.regular-expressions.info/) then those can be quite useful in cleaning up the list.

Note that Lantern's UI does not work ideally for bulk adding. You may get an 'invalid line' error. If you've got a long list it can be quite hard to find that line. The lantern UI will report that line, so we recommend copying that and then searching for it (like with ctrl-f, to do it automatically) in the program you pasted the list from. So it's best to work on your list outside of Lantern, then paste it in and keep editing until there are no more errors.


### Removing sites

We recommend scrolling through the list and removing any sites that you know are not blocked in your country. To remove sites just select them in the text field and hit 'delete'. Be sure to hit 'update' when you're done.

![update](https://www.evernote.com/shard/s209/sh/81bd9e5b-808c-4b3a-bb8f-487fee2601fd/bf5af2b060b92a44336a9ccc7ff8988b/deep/0/Lantern.png)

### Sharing

If you would like to share your list of proxied sites with a friend who's using Lantern, simply select all the sites you'd like to share with your mouse, or click inside the text box and hit Ctrl-A (Command-A on OS X) to select them all, copy them to the clipboard with Ctrl-C (Command-C), and paste them into an email to your friend using Ctrl-V (Command-V). Your friend can then copy the sites you sent her and then paste them into her Proxied Sites screen in Lantern.

If you'd like to share your list of proxied sites publicly, feel free to add them to a new page on the [Lantern Proxied Sites List Wiki](https://github.com/getlantern/lantern-proxied-sites-lists/wiki). Just click the green 'New Page' button, give your page a name, then on the Create New Page screen, paste your list in between two lines containing only three back-tick characters, like so:

\`\`\`

site1.com

site2.com

site3.com

\`\`\`

Feel free to add a post to the [User Forums](https://groups.google.com/group/lantern-users-en) with a link to the list you just created so other users can check it out!