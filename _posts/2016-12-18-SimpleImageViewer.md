---
layout: post
title: 画像を表示するシンプルなアプリ
---

### 概要
下記を参照に画像を表示するだけのシンプルなアプリを写経して作ってみました。

> https://iphone-app-tec.com/ios/uiimageview.html

### コード
```swift:ViewController.swift
import UIKit

class ViewController: UIViewController {
    
    override func viewDidLoad() {
        super.viewDidLoad()
        initImageView()
    }

    private func initImageView(){
        // UIImage インスタンスの作成
        let image1:UIImage = UIImage(named:"yagen")!
        // UImageView 初期化
        let imageview = UIImageView(image:image1)
        
        //画面の横幅を取得
        let screenWidth:CGFloat = view.frame.size.width
        let screenHeght:CGFloat = view.frame.size.height
        
        //画像の中心を画面の中心に設定
        imageview.center = CGPoint(x:screenWidth/2, y:screenHeght/2)
        
        //UIImageViewのインスタンスをビューに追加
        self.view.addSubview(imageview)
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }
}
```
