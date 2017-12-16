# Question Three (Android)

What is the output of the following code assuming that the catch block is not called and the picture.txt file returns the following text: "Hello there Cat":

```java
    import android.util.Log;
    import okhttp3.OkHttpClient;
    import okhttp3.Request;
    import okhttp3.Response;


    public class activity extends AppCompatActivity implements NavigationView.OnNavigationItemSelectedListener {

        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity);
            
            try {
                OkHttpClient client = new OkHttpClient();

                Request request = new Request.Builder()
                    .url("https://www.thisSitereturnsacatpicture.com/picture.txt")
                    .build();

                Response resp = client.newCall(request).execute();


                Log.d("Response", resp.body().toString())
            
            } catch(Exception e) {
                
            }

        }
    }

```

## Solving the question

The following are steps on how to submit a solution
 - Create a folder
 - Create files associated with the question you are solving in that folder
 - Once you have completed all the questions zip up the file and send it to me via messenger. 
