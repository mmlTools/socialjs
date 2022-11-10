# Social sharing buttons jquery plugin
 ![alt text](https://imgur.com/e7afx3e.png)

Create a sharing plugin for your current url; it is the simplest tool to utilize in a blog for allowing readers to share your material using the sharing API on numerous social media networks. The setup is quite simple, and all the parameters are shown below.

# Requirements

jQuery 3.x+ - https://releases.jquery.com/

Font Awesome 5.9 - https://cdnjs.com/libraries/font-awesome/5.9.0

Optional, Bootstrap - https://getbootstrap.com/

# Setting up the plugin

Create a div that represents the Block Wrapper of your social url sharing buttons
```html
<div id="MySharingButtonsWrapper"></div>
```

Append sharing links to the newly created sharing wrapper. This example is just a default global sharing plugin. You can pass what content you wish even PHP generated content.
```js
$('#MySharingButtonsWrapper').socialSharingPlugin({
        url: window.location.href,
        title: $('meta[property="og:title"]').attr('content'),
        description: $('meta[property="og:description"]').attr('content'),
        img: $('meta[property="og:image"]').attr('content'),
        responsive: true,
        mobilePosition: 'left',
        enable: ['copy', 'facebook', 'twitter', 'pinterest', 'linkedin', 'reddit', 'stumbleupon', 'pocket', 'email', 'whatsapp']
    })
```

# Sharing plugin configuration variables

| Parameter                | Default Value             | Description |
| -------------            | ---------------------     | ------------- |
| url                      | blank                     | Represents the url that is shared accros the social media platforms  |
| title                    | blank                     | Sharing message title  |
| description              | blank                     | Sharing message description  |
| img                      | blank                     | Usually open graph image  |
| btnClass                 | blank                     | CSS class to apply on the sharing buttons  |
| enable                   | null                      | Array of social sharing links to use on the website, available options are ['copy', 'facebook', 'twitter', 'pinterest', 'linkedin', 'reddit', 'stumbleupon', 'pocket', 'email', 'whatsapp']  |
| responsive               | false                     | Use responsive class on mobile devices  |
| mobilePosition           | left                      | Responsive class turn the wrapper to fixed position, you can set the placement to right and left  |
| copyMessage              | Copy to clipboard         | Message that appers on the tooltip for the copy link button  |

# JS URL parameters explained
| Parameter     | Description |
| ------------- | ------------- |
| [post-title]	| Message title |
| [post-url]    | Url sent inside your message|
| [post-desc]   | Description received from plugin init |
| [post-img]    | Open graph image |
