This project is an example of how RestKit can be used to talk directly to an ElasticSearch instance from ObjectiveC.

# Installation

* You may or may not have a ```dev``` folder, it is up to you, whereever you choose to work.

* ```
$ cd ~/dev/
$ git clone --recursive git://github.com/pulkitsinghal/ESClientDemo.git
```

* If you forget to provide the ```--recursive``` flag, you can always download the submodules in a later command using:

* ```
$ cd ~/dev/ESClientDemo/
$ git submodule update --init --recursive
```

* You must add `ESClientDemo/config.plist` in order to use the project out-of-the-box.

* ```
$ vi ~/dev/ESClientDemo/ESClientDemo/config.plist
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
        <key>protocol</key>
        <string>http</string>
        <key>address</key>
        <string>123.456.789.101</string>
        <key>port</key>
        <string>9200</string>
        <key>index</key>
        <string>index_name</string>
</dict>
</plist>
```

* If you have multiple clones and you use the same config across them all then simply soft link them.

* ```
$ cd ~/dev/ESAdditionalClone/
$ ln -s ~/dev/ESClientDemo/ESClientDemo/config.plist ./ESClientDemo/config.plist
```

* Launch the ```.xcodeproj```
* ```Set the active scheme``` to ESClientDemo
* Choose the simulator or device
* ```Run``` it!
