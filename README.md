# Hugo theme Objektiv

<img width="1427" height="720" alt="Screenshot 2026-02-18 at 18 49 30" src="https://github.com/user-attachments/assets/eb609906-fab4-4ddf-82b1-bb5e6a1c1f06" />

Welcome! This is a custom theme built for a friend. However, if you find the theme suitable for your needs, feel free to follow the intructions below to use the theme for yourself! This theme is free and open-source.

## How to start using this theme

> [!NOTE]
> These instructions assume you intend to use GitHub Pages as your host and does *not* require any need for local development. Instead, it relies on GitHub Actions to automatically rebuild the site any time you modify the repository's content. Note that this is not exactly the usual for working with Hugo sites, where most authors use Git to push changes from their local machine.

> [!NOTE]
> These instructions are intended for anyone to follow, regardless of technical background. If you have any problems setting up, feel free to open an issue.

---

The first thing you'll need to make sure you have is a GitHub account. Click [here](https://github.com/signup) to create one of you haven't already. You can also use an existing Google or Apple account.

> [!TIP]
> Choose  meaningful username, since it will appear in your website's url. For example, if you choose `PolarBear` as your username, your website's url will `https://polarbear.github.io`. Consider using your name in some way, unless you have a username with an established digital identity.

Once you've created an account, it's time to create a repository.

> ###### For my friend:
> As a new GitHub user, I was always intimidated at the terms like "repository". Actually, there's nothing to be afraid of. A repository, or a "repo", is simply a place where all your code for one project lives. On your own computer, that usually looks like a folder with a bunch of subfolders and code files. And on GitHub, it's no different. When you open a new repo, it's like creating a new folder on your computer. Simple!

Instead of creating a new repository and copying code files to it one by one, we'll do something a lot more efficient: we'll just make a fork of an existing one.

> ###### For my friend:
> A "fork" can also be a confusing term for beginners. A fork is nothing more than a copy of the original repository. When we fork a repository, we're basically making a special personalized copy of it for ourselves. If you've ever used the "spin-off" feature on Khan Academy, this is the exact same thing, but on GitHub.

First, make sure you're logged in to GitHub. Now head over to the repository we want to fork. Here's the [link](https://github.com/nicolasGreenwood/objektiv-starter-template).

Once you're there, click on the "fork" button in the upper right corner.

<img width="1377" height="671" alt="Screenshot 2026-02-18 at 19 17 26" src="https://github.com/user-attachments/assets/bea7eee5-ed67-4785-b4fe-ac82663e6b23" />

This will redirect you to a new page. Here, enter a name for your repo. This name should be your github username, + .github.io at the end. If your username is `PolarBear`, your repository name here should be `polarbear.github.io`.

Also write a short description, and then click "Create fork".

<img width="892" height="627" alt="Screenshot 2026-02-18 at 20 05 57" src="https://github.com/user-attachments/assets/6ba43c9a-8e27-470c-bacf-f1fc54f2f5fa" />

You will be redirected to a new page. This is the home page of your new repo! This is where your site's content and code will live.

Now, we need to do 2 more things: activate hosting for the site so your website becomes live on the internet, and add some new content to the site. Let's tackle the first one.

One the top bar, click on "Settings".

<img width="1420" height="728" alt="Screenshot 2026-02-18 at 20 10 08" src="https://github.com/user-attachments/assets/5da859e3-2a83-459c-8113-4a8160a6f499" />

Now, find "Pages" in the left side menu and click on it:

<img width="1421" height="730" alt="Screenshot 2026-02-18 at 20 11 19" src="https://github.com/user-attachments/assets/c184d7ea-a2d1-4c4d-b8fe-b6bc21973ae7" />

Under the "Source" dropdown, open it and select "GitHub Actions".

<img width="1416" height="722" alt="Screenshot 2026-02-18 at 20 14 44" src="https://github.com/user-attachments/assets/7c4c9780-0ce0-4b33-a868-685c24e08db7" />

That's it! Only a little more set-up to do. Let's talk about configuring your site. 

You may have noticed that your name is not appearing in that upper left corner when you visit the site. That's because you need to add your name in the site's settings. And where do the site's settings live? 

If you return to the home page of your site's repo, you'll see a file called hugo.yaml. This is where all the settings of the site live, just waiting for us to tweak them. Open it and click on the pencil icon to the right to edit it!

I've added explanations on each setting, so read them and change values them as needed. Try not to mess up the formatting—the YAML language is picky about it. When you've changed everything as you like it, click on "commit changes" and you're good to go! The site should reflect those updates you made in a short while.

Now let's add some content to your site!

To do that, go back to the home page of your repository. You should see a list of files and folders. One folder is called "content". Click on it. 

Here, you'll see several files and folders. 

- The _index.md (.md file extension simply means markdown) is the home page. No need to touch that.
- The about.md is the About page for your site. You can open that file and edit it to add some text about yourself.
- The contact.md is the Contact page for your site. As you guessed, you can write something here about your Contact page.
- The "journal" folder contains all your journal entries.
- The "poems" folder contains all your poems.

That's it! That's all your content.

Let's add a new poem. First, we'll open the "poem" folder. Then, we'll click on "add file". We'll name it something—the recommendation is to use the title of your poem, make it all lowercase, and replace all spaces with hyphens. And end it in ".md", because it's a markdown file.

Now, let's add some content to the poem. First, we need to define some metadata (data about data) for the poem. That includes stuff like the date, the title, the cover image and so on. EACH POEM/JOURNAL ENTRY has to have metadata! Without it, it won't be able to add your poem/journal entry to the site.

Here's the specific metadata you need to fill out. You can copy and paste this whole thing into your new file and just change the values as needed. I even added explanations for each parameter so you can't make a mistake :)

Oh, and don't forget to include those three hypens at the beginning and end of the metadata! It's what separates the metadata from your actual post content.

```yaml
---
title: My Lovely Title # Just a title, super easy. If you use a colon in title, enclose the whole thing in quotes.

date: 2026-01-02 # The date must be in this format: "YYYY-MM-DD". Other formats will result in an error.

draft: false # VERY IMPORTANT: switch this to "false" when you're ready to publish. Until then, this post will only remain in your content folder and not be published to the site.

summary: Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Ut non enim eleifend felis pretium feugiat. Vivamus quis mi. Phasellus a est. Phasellus magna. In hac habitasse platea dictumst. # Delete this dummy text above and write a short, catchy summary. Often an excerpt works really well.

tags: # List some tags here. These help you connect your posts with other related ones. Use as many as you like, but more importantly, the more posts share the same tag, the better.
    - walk
    - travel # ! Be sure to maintain indentation when you add tags!

params: 
    cover: images/entry-1-cover.jpg # This is an important parameter. This is the featured image that every post has! Find a nice one that's free to use. The best sites incluse unsplash.com, pixabay.com, pexels.com and even WikiMedia Commons if you're looking for historical/geographic photos. Don't just use random images off of Google, as some of them may not be free to use. Download the images, upload them to the static/images folder, and then link them here like this: /images/the-name-of-your-photo.jpg (or.png, or.webp, or whatever file extension your photo has.) And that's it!
---
```

Alright, filled that out? Time to write some poetry. Write it below the metadata, after the three-hypen line. Write as much as you like.

When you're finished, click on "commit changes". This will add your new poem to the site and trigger a rebuild of your site. Yes, your site is now being "built", so to speak, by Hugo and GitHub! It's applying all kinds of cool styles and formatting to your new poem.

After about 10 minutes max (but often after only 1-2 minutes), your site should display your new poem when you visit the url. Enjoy your first poem!

Adding a journal entry is the exact same process, except in the "journal" folder.

You might have noticed a "poem-template.md" and a "entry-template.md" in the poems and journal folders. Those are actually just regular posts too! They're there to serve as a simple template for all that metadata. You can edit them into another post, or keep them for reference. Just set "draft" to "true" in their metadata to prevent them from showing up on your live site if you do so.

This is how you add content to your site whenever you have a brilliant new poem sitting in your drawer, or want to jot a few notes down in your journal.

---

This is a complex set-up process for people who have never used GitHub before, so if you have any issues, or something isn't clear, please don't hesitate to contact me. You can open an issue, or if you're my friend, you can contact me in any other way as well. I can assure you you'll recieve a response as soon as I see your message.

Enjoy your new site! 
