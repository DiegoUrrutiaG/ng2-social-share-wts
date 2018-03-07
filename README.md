#Usage 

```javascript
npm install --save ng2-social-share
```


Made this, you should include the directive where you want to use it as any other Angular2 directive.

```typescript
import { Component, OnInit } from '@angular/core';
import { SocialShare } from 'ng2-social-share-wts';

@Component({
    selector: 'app-my-fancy-component',
    templateUrl: 'my-fancy-component.component.html',
    directives:[socialShare]

})
export class myFancyComponent implements OnInit {
//vars used only for example, put anything you want :)
public repoUrl = 'https://github.com/DiegoUrrutiaG/ng2-social-share-wts';
public imageUrl = 'https://avatars2.githubusercontent.com/u/10674541?v=3&s=200';

constructor() { }

ngOnInit() {
//do something OnInit

}

}
```

###Accepted params


```typescript

export declare class FacebookParams {
    u: string;
}

export class GooglePlusParams {
    url: string
}

export class LinkedinParams {
    url:string
}

export declare class PinterestParams {
    url: string;
    media: string;
    description: string;
}

export class TwitterParams {
    text: string;
    url: string;
    hashtags: string;
    via: string;
}

export class WhatsappParams {
    // url: string;
    text: string;
}

```

###In your component html file
 
 ```html

 <!--- For this example I am using button, but you can attach the directive to anything you want
    and it will display the popup for share! :D
 -->
    <button socialShare [facebook]="{u: repoUrl}">Facebook</button>
    <button socialShare [linkedIn]="{url:repoUrl}">Linkedin</button>
    <button socialShare [googlePlus]="{url:repoUrl}">Google Plus</button>
    <button socialShare [twitter]="{url:repoUrl, text:'Checkout this awesome ng2 social share directive', hashtags:'angular2, social'}">Twitter</button>
    <button socialShare [pinterest]="{url:repoUrl, media: imageUrl, description:'Checkout this awesome angular2 directive'}">Pinterest</button>
	<button socialShare [whatsapp]="{text: repoUrl}">Whatsapp</button>




 ```




###ROADMAP

    Support for:
    Email
    Telegram
    Viber
    Line
    Tumblr
    Hackernews
    VK
    XING
    Buffer
    Instapaper
    Pocket
    Digg
    Stumble Upon
    Flipboard
    Weibo
    Renren
    My Space
    Blogger
    Baidu
    Douban
    Okru
