# AndroidStarterTemplate
Android Application Starter Template

This repository contains an Android Template application built on the Android Native platform. The application contist of a User Interface with splashscreen, Login, and MainActivity with a Sliding Tab Layout combined with a tool bar. This template can be used start a new project or an existing project. The application also contains 3 tabs, each one is designated to their own tab. The Android application's design and color scheme coincide with the BootstrapTemplate. 

### The application has functional intents with activities

Inline-style: 
![device-2015-07-23-121529](https://cloud.githubusercontent.com/assets/11635523/8863558/a63f0b30-314e-11e5-90e8-87017b6d402f.png)
![device-2015-07-23-123514](https://cloud.githubusercontent.com/assets/11635523/8863574/c4aae7f6-314e-11e5-8b90-ef2466fc01e8.png)

Inline-style: 
![device-2015-07-23-122052](https://cloud.githubusercontent.com/assets/11635523/8863629/3b037c92-314f-11e5-9c34-e256ef25f8e5.png)
![device-2015-07-23-122144](https://cloud.githubusercontent.com/assets/11635523/8863662/6b7d5fdc-314f-11e5-9a1c-774c36f41136.png)


##If you wish to add more tabs

```java 
   CharSequence Titles[]={"Tab1","Tab2", "Tab3"};
    int Numboftabs =3;
```

```java 
 //This method return the fragment for the every position in the View Pager
    @Override
    public Fragment getItem(int position) {

        if(position == 0) // if the position is 0 we are returning the First tab
        {
            Tab1 tab1 = new Tab1();
            return tab1;
        }
        else if(position ==1){ // As we are having 2 tabs if the position is now 0 it must be 1 so we are returning second tab
            Tab2 tab2 = new Tab2();
            return tab2;
        }
        else{
            Tab3 tab3 = new Tab3();
            return tab3;
        }
    }
```

You will need to create a new activity, for example Tab4. The **CharSequence** strings will need to be modified "Tab4" You will need to modify **int Numboftabs**  = "4" this is given for the specific number of tab activities that are in use for the Sliding Tab Layout. 
The conditional statement will also need to be modified to fit with the new set of Tab(s). You can modify this is by setting up a swtich statement for the conditionals or any other type of method. 

###Switch statement method
This is the conditional statement that can be used for adding more that 3 tabs. 
```java 
 //This method return the fragment for the every position in the View Pager
    @Override
    public Fragment getItem(int position) {
        switch (position) {
            case 0:
                return new Tab1();
            case 1:
                return new Tab2();
            case 2:
                return new Tab3();
            case 3:
                return new Tab4();
            case 4:
                return new Tab5();
        }

        return null;
    }
```



##If you decide to use it 
Make sure to add your package name to the Sliding Tab Layout in the activity_main.xml file

```xml 
<com.example.android.androidtemplate.SlidingTabLayout
        android:id="@+id/tabs"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@color/ColorPrimary"/>
```

From **com.example.android.androidtemplate.SlidingTabLayout**
To
**com.example.android.packagename.SlidingTabLayout**
This is only needed if you decide to add it to an already existing project.


##How to Use
```git

  $ git clone https://github.com/JonathanMoreno14/AndroidStarterTemplate.git
   
```


The Sliding Tab Layout was inspired and part of a tutorial segment from  [Android For Devs] (http://www.android4devs.com/2015/01/how-to-make-material-design-sliding-tabs.html) .

