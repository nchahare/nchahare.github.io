---
title: "Zotero: How to sync files"
author: Nimesh Chahare
layout: post
date: 2023-10-29
description: Using zotfile to sync PDFs across multiple devices
tags: resources
authors:
  - name: Nimesh R. Chahare
    url: "https://nchahare.github.io"
    affiliations:
      name: IBEC Barcelona
toc:
  - name: Understanding Zotero's Data and Files
  - name: Default Zotero Syncing
  - name: Setting Up Zotero Sync
  - name: Syncing Your Library to a New Computer
  - name: Managing File Syncing
  - name: Exploring Zotfile for File Syncing
  - name: Syncing Across Multiple Computers
  - name: References
---

# How to Sync Files in Zotero

Zotero is a powerful reference management tool that allows you to organize and access your research materials with ease. While it primarily stores reference data, it's important to understand that you can also sync files such as PDFs to your library. If you compare it with Mendeley, **it only has 300MB of online storage**. In this tutorial, we'll show you how to effectively sync your Zotero library, including PDFs, across multiple devices.

## Understanding Zotero's Data and Files

Before we dive into the syncing process, it's crucial to differentiate between two core components of Zotero:

1. **Data**: This includes reference information, notes, paper titles, and other metadata, but not PDFs.
2. **Files**: These are the PDFs and other attachments that you attach to your references.

## Default Zotero Syncing

By default, Zotero stores both data and files locally on your computer. However, Zotero offers a syncing feature that allows you to access your library on any computer with internet access.

## Setting Up Zotero Sync

1. **Create a Zotero Account**: If you don't have one already, sign up for a Zotero account on their website.

2. **Access Sync Preferences**:
   - Open Zotero and go to the top bar.
   - Click on "Edit" and select "Preferences."
   - In the "Sync" section, you can enter your account information.

3. **Initiate Sync**:
   - After adding multiple references in the library
   - In your Zotero library, click the circular green arrow to start the sync process.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231029124616.jpg" title=" " class="img-fluid rounded z-depth-1" %}
</div>

## Syncing Your Library to a New Computer

Once you've set up syncing on one computer, you can easily access your Zotero library on another computer.

1. **Login**: On the new computer, log in using your Zotero username and password.
2. **Instant syncing**: Your references and data will be populated instantly on your new device.

## Managing File Syncing

Zotero's syncing allows you to choose what to sync. It's important to note that the storage space available on the Zotero server is limited to 300MB, which can be quickly filled if you sync PDFs.

To manage this:

1. **Data Syncing Only**:
   - To conserve space, consider syncing only the data (references, notes, etc.) and not the files (PDFs).
   - Uncheck the "File Syncing" option in the Sync preferences.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231025084203.png" title=" " class="img-fluid rounded z-depth-1" %}
</div>

2. **Checking Your Data Usage**:
   - You can check how much data you are using by going to "zotero.org," logging in, and accessing your storage settings.

3. **Clearing PDF Data**:
   - If you've mistakenly added too many PDFs, you can press the red button in your Zotero settings to remove the PDF data from the Zotero cloud. You will still retain the PDFs on your device but won't access them through the web library.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231029123629.png" title=" " class="img-fluid rounded z-depth-1" %}
</div>

## Exploring Zotfile for File Syncing

Zotero offers 300MB of free storage for basic syncing. If you require more space for syncing your PDF articles without purchasing extra storage, you can use Zotfile, which combines Zotero's default sync service with an external storage solution, such as OneDrive, Google Drive, or Dropbox.

### Using Zotfile for Free File Syncing

Follow these steps to set up Zotfile for file syncing:

1. **Download Zotfile**:
   - Visit [zotfile.com](http://zotfile.com) to download the Zotfile extension.

2. **Installation**:
   - Open Zotero and go to "Tools" > "Add-ons."
   - Drag and drop the Zotero XPI file you downloaded and then install and restart Zotero.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231029125406.png" title=" " class="img-fluid rounded z-depth-1" %}
</div>

3. **Set Up Base Directory**:
   - Go to "Zotero" > "Preferences" > "Advanced" > "Files and Folders."
   - Choose a base directory in your OneDrive (or other cloud storage) where Zotero will store your PDFs. Create a folder and name it "Zoterodb." For example.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231029125457.jpg" title=" " class="img-fluid rounded z-depth-1" %}
</div>

4. **Custom Location**:
   - In "Tools," go to "ZotFile Preferences" and choose the "Zoterodb" folder as the custom location.

<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/Pasted image 20231029125557.jpg" title=" " class="img-fluid rounded z-depth-1" %}
</div>

With Zotfile, your PDFs will be automatically renamed and moved to the designated folder in your cloud storage whenever you add a new article. 

For your previous articles, select all and right-click, and choose "Manage Attachments," then rename and move them. This way, all of the articles will be moved into your OneDrive "Zoterodb" folder. 

It's a convenient way to expand your syncing capabilities.

## Syncing Across Multiple Computers

If you want to access your Zotero library on another computer while using Zotfile, follow these steps:

1. **Log In**:
   - Log in to your Zotero sync account, which you set up on your previous computer.

2. **Synchronize Database**:
   - Your Zotero database will be synchronized, but keep in mind that this doesn't include attachment PDFs. You won't be able to see the PDFs with your articles on the new computer.

3. **Set Up Shared Directory**:
   - Install the cloud storage application (e.g., OneDrive) on your new computer.
   - Share the "Zoterodb" folder from your previous computer and add it to your new computer. Remember that the folder's location may be different on both computers.

4. **Configure Base Directory**:
   - In Zotero, go to "Preferences" > "Advanced" > "Files and Folders."
   - Set up the base directory, which should be the shared directory on your cloud storage (e.g., OneDrive).

5. **Custom Location**:
   - In "Tools," access "ZotFile Preferences" and select the "Zoterodb" folder as the custom location.

Now, both of your computers will sync PDFs and attachments, offering a convenient and free way to access your research materials across different devices.

By following these steps, you can make the most of Zotero's syncing capabilities and ensure that your research library is accessible from anywhere, while efficiently managing your storage space.

## References

- Zotero help section: [https://www.zotero.org/support/preferences/sync#file_syncing](https://www.zotero.org/support/preferences/sync#file_syncing)
- Big thanks to this guy for teaching me zotfile. [https://youtu.be/MfFXQ5JYPeA?si=ctgNQkwj_--2ncnF](https://youtu.be/MfFXQ5JYPeA?si=ctgNQkwj_--2ncnF)
