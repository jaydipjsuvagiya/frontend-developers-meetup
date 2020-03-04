# FED Meetup Chapter - Feb 2020

**Point Covered**
* Web Performance
  * [Media optimasation](#media-optimisation)
  * [Reduce HTTP calls](#reduce-http-calls)
  * [Third party hosting for assets](#third-party-hosting-for-assets)
  * [Lazy loading of media](#lazy-loading-media)
* Project Structure
  
  
    
## Web Performance
Now days, as a frontend developer we need to think about web performance also, because this is the most important part of our work life. as we all know, making website is not a big deal but the real challenge is making a website which can load faster even in a slower network.  
  
 Here are some points we need to take care of while developing a website/web app  
  
#### Media optimisation
we are using following types of media in website in form of Image and SVG. so we can use (below Listed) website/tools for optimisation  
  
**Image**  
[tiny png](https://tinypng.com), [img optim](https://imageoptim.com/mac)  
    
**SVG**  
[svgomg](https://jakearchibald.github.io/svgomg), [svg go](https://github.com/svg/svgo)  
  
#### Reduce HTTP calls
To reduce less http calls we need to organised our css and js files properly and with usage of some good bundler like [Webpack](https://webpack.js.org/), [Parcle](https://parceljs.org/), [Laravel Mix](https://laravel-mix.com/docs/5.0/installation) we can make bundles of our css and js files.

#### Third party hosting for assets
It's good to host images and videos to another server and use them as a CDN to our project. because dedicated third party hosting service like [Cloudinary](https://cloudinary.com/), [Amazon cloudfront](https://aws.amazon.com/cloudfront/) made to provide your asset speedily, already have good servers and optimised structure for delivering asset.  
yes it increase our cost :D    

#### Lazy loading media
Load all images/iframes eagerly is making high impact on website loading time. so it's good to load all images and iframe when it actually came into view port and it also reduce our HTTP call.
there are many way to do this using javascript like [Lazy Loading](https://css-tricks.com/snippets/javascript/lazy-loading-images/)  
  
  we can do this [natively](https://web.dev/native-lazy-loading/) also, but it's not fully supported by all browser [see here](https://caniuse.com/#feat=loading-lazy-attr) 


## Project Structure
We can manage our scss structure like this [click here](https://www.sitepoint.com/architecture-sass-project/)  
  
*Please note that all things we discussed/referred is our own way to get work done. this is not recommended/useful in all cases so think about what fits best to you*
