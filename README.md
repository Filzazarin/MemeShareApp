## MemeShareApp
- Meme Share app is Funny app where user can see Funny memes on app.
- User will react on that Memes by sharing it on all the social media present in your andriod. 
- User having next feature also.
## Functionality
- Application uses API calls to retrieves memes from the internet and display it.
- Fetches memes via Volley Library from Reddit API and render via glide library.

 JSON API for a random meme scraped from reddit.

  - API Link : https://meme-api.herokuapp.com/gimme


## Use Gradle
```
repositories {
  google()
  mavenCentral()
}

dependencies {
  implementation 'com.github.bumptech.glide:glide:4.13.0'
  annotationProcessor 'com.github.bumptech.glide:compiler:4.13.0'
}
```
## Singleton class that provides RequestQueue.
Volley provides a convenience method Volley.newRequestQueue that sets up a RequestQueue for you, using default values, and starts the queue. 
```
class MySingleton constructor(context: Context) {
    companion object {
        @Volatile
        private var INSTANCE: MySingleton? = null
        fun getInstance(context: Context) =
            INSTANCE ?: synchronized(this) {
                INSTANCE ?: MySingleton(context).also {
                    INSTANCE = it
                }
            }
    }
    val requestQueue: RequestQueue by lazy {
        // applicationContext is key, it keeps you from leaking the
        // Activity or BroadcastReceiver if someone passes one in.
        Volley.newRequestQueue(context.applicationContext)
    }
    fun <T> addToRequestQueue(req: Request<T>) {
        requestQueue.add(req)
    }
}
```

