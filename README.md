## MemeShareApp
- Meme Share app is Funny app where user can see Funny memes on app.
- User will react on that Memes by sharing it on all the social media present in your andriod. 
- User having next feature also.
## Functionality
- Application uses API calls to retrieves memes from the internet and display it.
- Fetches memes via Volley Library from Reddit API and render via glide library.

## Use Gradle
```repositories {
  google()
  mavenCentral()
}

dependencies {
  implementation 'com.github.bumptech.glide:glide:4.13.0'
  annotationProcessor 'com.github.bumptech.glide:compiler:4.13.0'
}

