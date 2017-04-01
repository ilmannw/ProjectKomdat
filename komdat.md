<h1 align="center"><img src="C:\Users\User\Desktop\New folder/alah.png"></h1>

<center>[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
</center>



# Sekilas Tentang
[`^ kembali ke atas ^`](#sekilas-tentang)

**Dotclear** is an open-source web publishing software published in 2003 by Olivier Meunier. A one man's project at first, Dotclear soon gathered a team comprising different personalities with various backgrounds.

The project's purpose is to provide a user-friendly tool allowing anyone to publish on the web, regardless of their technical skills.

Dotclear is a free software primarily designed for its users and regularly improved by their contributions. Everyone may use it and modify it according to the [software license](https://dotclear.org/license).



# Instalasi
[`^ kembali ke atas ^`](#)

#### Kebutuhan Sistem :
Dotclear 2 requires a few specifications to work properly. Most of web hosting providers offer them. These specifications include:

- PHP 5.3 or more recent version, with the following extensions:
	- mbstring
	- iconv
	- simpleXML et domXML
	- SPL

- A supported database among the following:
	- PostgreSQL 8.0 minimum
	- MySQL 4.1 minimum avec InnoDB
	- SQLite

#### Proses Instalasi :
1. Login into server using SSH. For windows user can use [PuTTY](http://www.putty.org/).
    ```
    $ ssh root@210.16.120.17
    ```

2. Make sure that all system packet *up-to-date*, then install all of system needs, like `Apache`, `PHP`, and `MySQL`.
    ```
    $ sudo apt-get update
    $ sudo apt-get install apache2
    $ sudo apt-get install mysql-server
    $ sudo apt-get install php
    $ sudo apt-get install libapache2-mod-php
    $ sudo apt-get install php-mysql
    $ sudo apt-get install php-gd php-mcrypt php-mbstring php-xml php-ssh2
    $ sudo service apache2 restart
    ```

3. Now start the Apache web server with the following command. 
    ```
    $ /etc/init.d/apache2 start
    ```

4. Utilize the following command to create database for Dotclear application.
    ```
    $ mysql -u root
    mysql> CREATE DATABASE dotclear;
    mysql> exit
    ```

5. Then change the directory into /var/www/html/
    ```
    $ cd /var/www/html/
    ```

6. Now its time to Dotclear package with the respective link.
    ```
    $ wget http://download.dotclear.org/latest.tar.gz
    ```

7. Immediately extract the downloaded package with 'tar' command.
    ```
    $ tar -xvzf latest.tar.gz
    ```

8. Again you need to change directory into Dotclear. Then add the write permissions for the following directories.
    ```
	$ chmod a+w cache/
    $ chmod a+w inc/
    $ chmod a+w public/
    ```

9. Restart kembali Apache web server.
    ```
    $ sudo service apache2 restart
    ```

10. Open the web browser and navigate to http://localhost/dotclear.
	
    - Set the Database information as shown below,

      ![1](https://www.linuxhelp.com/post_screenshots/7102/1272.png)

    - Next enter the following details to create user for Dotclear.

      ![2](https://www.linuxhelp.com/post_screenshots/7102/2187.png)

    - Click on Manage your blog now option to complete the installation process.

      ![3](https://www.linuxhelp.com/post_screenshots/7102/3121.png)

    - Once the Dotclear is installed, open the Dashboard to view the advanced features as shown below,

      ![4](https://www.linuxhelp.com/post_screenshots/7102/4103.png)



# Konfigurasi
[`^ kembali ke atas ^`](#)

Dotclear can be extended in many ways with virtually no limits. Our main principle is to keep Dotclear simple and let users expand what Dotclear can do thanks to a simple and efficient framework.s

![1](C:\Users\User\Desktop\New folder/11.png)

### Plugins
- Many plugins can be installed to add extra features to the core functionality of your blog. You can also find them on Dotaddict.org.

    ![modul](C:\Users\User\Desktop\New folder/12.png)

- You can setting or manage your web's plugins in tab "Plugins" on admin dashboard

	![ada](C:\Users\User\Desktop\New folder/14.png)
    
### Themes
- Dotaddict.org lets you search and download many user-contributed themes so you can find the look and feel that best suits your taste and needs.

    ![design](C:\Users\User\Desktop\New folder/13.png)

- This is steps in how to change your web's theme :
	1. Click menu "Blog Appearance" on sidebar
	![da](C:\Users\User\Desktop\New folder/16.png)
    
    2. Choose the theme that you want and then there will be notification
    ![ads](C:\Users\User\Desktop\New folder/17.png)
    
    3. Congratulation your theme has been applied!
    ![asda](C:\Users\User\Desktop\New folder/18.png)


# Maintenance
[`^ kembali ke atas ^`](#)

When our web application has been installed, we can maintenance our application in purpose to keep our site nice and tidy. Dotclear also has this feature and this is a default feature. This is how it goes :

1. Click "Maintenance" on tab "Plugins"
    
    ![dashboard](C:\Users\User\Desktop\New folder/19.png)

2. In this feature, you can either "Servicing", "Backup", or "Setting Alert" your site
    ![shop](C:\Users\User\Desktop\New folder/20.png)
    
    ![13](C:\Users\User\Desktop\New folder/21.png)
    
	![12](C:\Users\User\Desktop\New folder/22.png)
    
3. Click **Execute Task** to save the changes.



# Otomatisasi
[`^ kembali ke atas ^`](#)

### Automatic Install

Using Dotclear 2's automatic installer is the easiest way to install the blog engine. It will check that PHP 5 is enabled, and if it's not, it will activate it for you. Then the files required to install Dotclear will be downloaded. You will then be redirected to the standard installation wizard to complete the process.

To install Dotclear using the automatic installer:

- Connect to your server through FTP
- Download [dotclear-loader.php](https://download.dotclear.org/loader/dotclear-loader.php) to your hard drive then transfer it to your server.
- Go to this file using your web browser (for example [www.example.com/dotclear-loader.php](http://www.example.com/dotclear-loader.php)).
- You may change the installation directory and leave this field untouched if you don't know what it is.
- Click on the button.

If everything goes fine, you'll only have to click on the Next button to access the Installation Wizard. If you encounter any issues, you will have to use the "standard" method described above.

### Automatic Update

NEW When a new version is available, you will be notified by a message on your dashboard and prompted to upgrade Dotclear. All you have to do is follow the instructions. The application will do the necessary checks and update the relevant files. You will then be asked to log out to complete the update. You will have nothing else to do, excepted maybe to check that your plugins still work properly.


# Cara Pemakaian
[`^ kembali ke atas ^`](#)

### Screenshot of Web Application
- Login Page
![login](C:\Users\User\Desktop\New folder/Capture.png)

- Admin Page
![admin](C:\Users\User\Desktop\New folder/Capture2.png)

- Site Page
![Site](C:\Users\User\Desktop\New folder/Capturee.png)

- Post Entry Page
![Post](C:\Users\User\Desktop\New folder/Capture4.png)


### Main Function of Web Application
1. Create a post entry

- Click "New Entry" option on the sidebar
![1](C:\Users\User\Desktop\New folder/1.png)

- Type the title of the post, then the content
![2](C:\Users\User\Desktop\New folder/2.png)

- Click image icon to insert an image in your post
![3](C:\Users\User\Desktop\New folder/3.png)

- Upload the image from your device
![4](C:\Users\User\Desktop\New folder/4.png)

- After the image uploaded, select image which will be inserted into post
![5](C:\Users\User\Desktop\New folder/5.png)

- Setting some adjustment on image then click insert
![6](C:\Users\User\Desktop\New folder/6.png)

- When you finished typing your post, change the "pending" status to "published", then click save
![7](C:\Users\User\Desktop\New folder/7.PNG)
![8](C:\Users\User\Desktop\New folder/8.PNG)

- If the post has been published, there will be notification on the top-right corner. To see the post you can click "go to this entry on the site"
![9](C:\Users\User\Desktop\New folder/9.PNG)
![10](C:\Users\User\Desktop\New folder/10.PNG)

2. Make Comment on Post

- Insert name and email address on Comment section
![12](C:\Users\User\Desktop\New folder/23.PNG)

- Click Preview button to see what's your comment look like
![213](C:\Users\User\Desktop\New folder/24.PNG)

- Click Send to publish

3. Delete Comment on Post

- Click on menu "Comment" to see all comments in your site
![w4](C:\Users\User\Desktop\New folder/25.PNG)

- Select which comment that you want to delete, change selected comment action from publish to delete then click ok
![2](C:\Users\User\Desktop\New folder/27.PNG)

- After that there will be notification if your comment has been deleted
![q23](C:\Users\User\Desktop\New folder/28.PNG)

4. Change Site Information

- Click "Blog Setting" menu on the sidebar
![23](C:\Users\User\Desktop\New folder/29.PNG)

- Insert the title and description of your site
![24](C:\Users\User\Desktop\New folder/30.PNG)
![2431](C:\Users\User\Desktop\New folder/31.PNG)

- Adjust any other settings like blog configuration and blog presentation
![13](C:\Users\User\Desktop\New folder/32.PNG)
![23](C:\Users\User\Desktop\New folder/33.PNG)

5. Add Widget

- Click "Presentation Widget" on sidebar
![234](C:\Users\User\Desktop\New folder/34.PNG)

- Choose the widget that you want in Available Widgets
![13](C:\Users\User\Desktop\New folder/35.PNG)

- Drag the widget to the right part, here you can choose where to place the widget
![3](C:\Users\User\Desktop\New folder/36.PNG)

- You can setting your widget by clicking the arrow icon of the widget
![34](C:\Users\User\Desktop\New folder/37.PNG)

- If you done, click update sidebars
![234](C:\Users\User\Desktop\New folder/38.PNG)

6. Add Pages

- Click menu "Pages" on sidebar
![131](C:\Users\User\Desktop\New folder/39.PNG)

- On the upper right corner click new page
![13](C:\Users\User\Desktop\New folder/40.PNG)

- After that, fill your pages title and content
![13](C:\Users\User\Desktop\New folder/41.PNG)

- When you've done, click save
![12](C:\Users\User\Desktop\New folder/42.PNG)

7. Add Tag and Categories

- Click menu "Categories" on sidebar
![23](C:\Users\User\Desktop\New folder/43.PNG)

- Click "New Category"
![23](C:\Users\User\Desktop\New folder/44.PNG)

- Fill the information of category that you want then click save
![23](C:\Users\User\Desktop\New folder/45.PNG)

# Pembahasan
[`^ kembali ke atas ^`](#)

Dotclear possesses a rich functionality that makes it a high quality publishing tool, equaling and even outperforming other similar tools in some aspects. Beyond the core functionality, Dotclear is designed to provide the user with the most comfortable experience. Features :
- **Easy publication** - Entries are written in a feature-rich editor allowing the user to add formatting to heir content. A wysiwyg editor is also available and completes a toolbox designed for easy publication, so that you can fully focus on what you are writing
- **Fully customizable theme** - You don't know what HTML and CSS are? Don't panic, you can customize the default theme online in every aspect (colors, fonts, header image, etc.) without touching a single line of code. Customizing your site has never been so easy.
- **User-friendly administration** - You should be able to write an entry quickly, without going through lengthy steps. The administration interface is easy to use and designed with the users in mind, regardless of their levels, without compromising on the functionality.Diterjemahkan dalam banyak bahasa, termasuk Bahasa Indonesia.
- **Media management** - You can add any kind of file to the media manager. The media manager will help you find your files when you want to include them in an entry. You can also include music and video from external services (e.g. Youtube, Deezer, etc.), by simply specifying the URL of the page that hosts the media to be included.
- **Presentation widgets** - The navigation elements of your blog can be customized through presentation widgets that you can place where you want them to be displayed, so you have full control on your layout. You can also use widgets to display all kinds of information (weather forecast, free text, rankings, etc.).
- **Themes and plugins** - You can install plugins to extend your blog's functionality, and themes to change its design. You will find all those resources on Dotaddict.
- **Multiblog** - A single Dotclear installation natively allows you to create as many blogs as you like, be it one, ten or thousands, without requiring a third-party application.
- **Naturally optimized for search engines** - The pages generated by Dotclear are designed for optimal — and relevant! — search engine visibility. Options are also available if you want to control or prevent the indexation of your content.
- **Twice free** - Dotclear is free to download and free to use


The advantages of Dotclear :
- Easy publication
- Package engine allows 1-click install for plug-ins and themes
- Fully customizable theme
- User-friendly administration
- Low requirements (PHP4/MySQL4) help to minimize hosting dependencies
- Flexible comment system
- Performance and scalability
- Huge number of available plug-ins

Dotclear also has disadvantages, there are :
- Single-site only
- Rudimentary security features
- Not suitable for large enterprise projects
- Very limited assets manager

Difference with similiar web application :

- Dotclear didn't cost many space, because it's only take about 4.48 MB in hosting.
- Simple and lightweight web app, anything that you do in Dotclear feel light and fast
- Permalink dotclear enable you to change repeatedly on drafting a post
- Powerfull, easy to use/user friendly, and trusted


# Referensi
[`^ kembali ke atas ^`](#)

1. [About Dotclear](https://dotclear.org/) - Dotclear
2. [How to install dotclear in Ubuntu](https://www.linuxhelp.com/how-to-install-dotclear-in-ubuntu/) - Linuxhelp
3. [Advantages and Disadvantages of Dotclear](http://www.monitis.com/blog/18-open-source-content-management-systems-part-3/) - monitis

