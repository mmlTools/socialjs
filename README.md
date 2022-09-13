# Social sharing buttons jquery plugin
 
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
$('#Demo').socialSharingPlugin({
   urlShare: window.location.href, // Takes the current URL
   description: $('meta[name=description]').attr('content'), // Retrieves the content of the current meta description
   title: $('title').text() // Retrieves the content of the current title tag
})

/* All available parameters */
$('#Demo').socialSharingPlugin({
    urlShare: '',
    btnTarget: '_blank',
    btnTitle: 'Share on',
    title: '',
    description: '',
    via:'',
    hashtags: '',
    img: '',
    isVideo: 'false',
    buttonClass: 'btn btn-light',
    applyDefaultButtonStyle: true
})
```

# Sharing plugin configuration variables

| Parameter                | Default Value | Description |
| -------------            | ------------- | ------------- |
| urlShare                 | blank         | Represents the url that is shared accros the social media platforms  |
| btnTarget                | _blank        | Wether if you want your user to stay on the page after clicking the button or open a new window  |
| btnTitle                 | Share on      | Link title attribute for SEO purpose  |
| title                    | blank         | Sharing message title  |
| description              | blank         | Sharing message description  |
| via                      | blank         | Twitter profile  |
| hashtags                 | blank         | Hash tags used on twitter  |
| img                      | blank         | Usually open graph image  |
| isVideo                  | 'false'       | String, true or false depending if the main url is a video or a normal URL  |
| buttonClass              | btn btn-light | Sharing button class for easier styling through your main CSS  |
| applyDefaultButtonStyle  | true          | Boolean, wether to apply icon color by default or you want to modify it in CSS, required if you wish to avoid using the nasty !important flag in CSS  |

# JS URL parameters explained
| Parameter | Description |
| ------------- | ------------- |
| [post-title]	| Message title |
| [post-url]    | Url sent inside your message|
| [post-desc]   | Description received from plugin init |
| [post-img]    | Open graph image |
| [is_video]    | Wether the post is a video or not |
| [hashtags]    | Hashtags for twitter |
| [via]         | Twitter user tag |