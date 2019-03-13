# Activity的生命周期

1.生命周期状态

  Activity生命周期指的是一个从创建到销毁的全过程。Activity的生命周期分为5种状态，分别是启动状态、运行状态、暂停状态、停止状态和销毁状态，
  其中启动状态和销毁状态是过渡状态，Activity不会在这两个状态停留。

2.生命周期方法

  Activity的生命周期主要涉及7种方法，分别是onCreate(),onStart(),onResume(),onPause(),onStop(),onDestroy(),onRestart()方法。
  
  ![Image text](https://raw.githubusercontent.com/1045896802/ActivityLife/master/img/1.png)
  
3.验证Activity的生命周期
  
  通过Activity涉及到的7种方法来验证Activity的生命周期，关键代码如下所示：

    public class MainActivity extends AppCompatActivity {

      private final String TAG = "MainActivityLife";

      @Override
      protected void onCreate(Bundle savedInstanceState) {
          super.onCreate(savedInstanceState);
          setContentView(R.layout.activity_main);
          Log.d(TAG, "onCreate()");
      }

      @Override
      protected void onStart() {
          super.onStart();
          Log.d(TAG, "onStart()");
      }

      @Override
      protected void onResume() {
          super.onResume();
          Log.d(TAG, "onResume()");
      }

      @Override
      protected void onPause() {
          super.onPause();
          Log.d(TAG, "onPause()");
      }

      @Override
      protected void onStop() {
          super.onStop();
          Log.d(TAG, "onStop()");
      }

      @Override
      protected void onDestroy() {
          super.onDestroy();
          Log.d(TAG, "onDestroy()");
      }

      @Override
      protected void onRestart() {
          super.onRestart();
          Log.d(TAG, "onRestart()");
      }


    }

4.实验结果
    如下图所示：
![Image text](https://raw.githubusercontent.com/1045896802/ActivityLife/master/img/2.png)
