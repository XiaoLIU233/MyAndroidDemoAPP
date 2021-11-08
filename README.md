# MyDemoAndroidAPP
This is my demo Android Application for 【Notification Tutorial】. See the Youtube link - https://www.youtube.com/watch?v=tTbd1Mfi-Sk&list=PLrnPJCHvNZuCN52QwGu7YTSLIMrjCF0gM&index=1

I outlined all the Android knowledge used in this project for future review as follows:
1.  <!-- Name of the method in this View's context to invoke when the view is
                 clicked. This name must correspond to a public method that takes
                 exactly one parameter of type View. For instance, if you specify
                 <code>android:onClick="sayHello"</code>, you must declare a
                 <code>public void sayHello(View v)</code> method of your context
                 (typically, your Activity). -->
     <attr name="onClick" format="string" />

2.  <!-- The SDK version of the software currently running on this hardware device. This value never changes while a device is booted, but it may increase when the hardware manufacturer provides an OTA update.
    Possible values are defined in Build.VERSION_CODES. -->
    public static final int SDK_INT = SystemProperties.getInt("ro.build.version.sdk", 0);

3.  <!-- The SDK version of the software that initially shipped on this hardware device. It never changes during the lifetime of the device, even when SDK_INT increases due to an OTA update.
    Possible values are defined in Build.VERSION_CODES. -->
    public static final int FIRST_SDK_INT = SystemProperties.getInt("ro.product.first_api_level", 0);

4.  /**
     * Min notification importance: only shows in the shade, below the fold. This should not be used with Service.
     * startForeground since a foreground service is supposed to be something the user cares about so it does not make semantic sense to mark its notification as minimum importance.
     * If you do this as of Android version Build.VERSION_CODES.O, the system will show a higher-priority notification about your app running in the background.
     */
     public static final int IMPORTANCE_MIN = 1;

    /**
     * Low notification importance: Shows in the shade, and potentially in the status bar
     * (see {@link #shouldHideSilentStatusBarIcons()}), but is not audibly intrusive.
     */
    public static final int IMPORTANCE_LOW = 2;

    /**
     * Default notification importance: shows everywhere, makes noise, but does not visually
     * intrude.
     */
    public static final int IMPORTANCE_DEFAULT = 3;

    /**
     * Higher notification importance: shows everywhere, makes noise and peeks. May use full screen
     * intents.
     */
    public static final int IMPORTANCE_HIGH = 4;