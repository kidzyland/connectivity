## Connectivity Manager

An Android Library for checking Internet state.


# Add Library

1. Add the JitPack repository to your build file
```groovy
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}
```

2. Add the dependency
```groovy
dependencies {
    .
    .
    .
    implementation 'com.github.kidzyland:connectivity:1.1.0'
}
```


# How to use 

Call initialization function in application class. It is better to use applicationContext to observe connectivity manager while application is running. 
Although you can use activity context if you want to observe connectivity state in specific activity.
```groovy

class MyApplication : Application() {

    override fun onCreate() {
        super.onCreate()
      
        CheckConnectivityModule.initialize(applicationContext)
    }
}

```

Call checkHasConnectionAndInternet function to check the connectivity state.

```groovy

val connectionState: CheckConnectivityModule.ConnectivityState =
            CheckConnectivityModule.checkHasConnectionAndInternet()

```

Return variable has three state : 

```groovy

NOCONNECTION --> connectiivty has disabled

HASINTERNET -->  connected to Internet

NOINTERNET --> not connected to Internet

```



## Licenses
```
Copyright 2019 Kidzy Land.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
```



