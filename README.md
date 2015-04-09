# FakeCodeSign-Xcode6
Run iOS app on a real device without a developer program.

### 1. 修改两个文件

1. Info.plist(位置：Xcode/Contents/Developer/Platforms/iPhoneOS.platform/Info.plist)
![0](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/0.png)

2. SDKSettings.plist(位置：Xcode/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/SDKSettings.plist)
![1](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/1.png)

### 2. 写App

比如写一个Button链接到ViewController.swift中的showMessage()方法的iPhone Swift App
```
@IBAction func showMessage() {
        let alertController = UIAlertController(title: "Congratulations", message: "Running on a real device...", preferredStyle: UIAlertControllerStyle.Alert)
        alertController.addAction(UIAlertAction(title: "OK", style: UIAlertActionStyle.Default, handler: nil))
        self.presentViewController(alertController, animated: true, completion: nil)
    }
```

### 3. 修改信息

1. Deployment Target
![2](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/2.png)

2. Code Signing
![3](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/3.png)

3. Entitlements.plist
![4](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/4.png)
![5](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/5.png)
![6](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/6.png)

### 4. Run on iOS Device

![7](https://raw.githubusercontent.com/zuzhi/FakeCodeSign-Xcode6/master/images/7.png)

### 5. Support or Contact

@zuzhi
