# CocoapodsTutorial

## [Cocoapods 官方連結](https://guides.cocoapods.org)

## 簡易的流程介紹

### 安裝

1. 安裝Cocoapods
    
  ```no-highlight
  sudo gem install cocoapods
  ```

2. 到專案資料夾產生podfile

  ```
  pod init
  ```

3. 編輯podfile

  ```
  target 'MyApp' do
    use_frameworks!
    pod 'Alamofire', '~> 3.0'
  end
  ```
  
4. 開始安裝pod裡頭定義的frameworks

  ```
  pod install
  ```
  
5. 執行透過pods產生出來的xcworkspace

### 移除

  ```
  sudo gem install cocoapods-deintegrate cocoapods-clean
  pod deintegrate
  pod clean
  rm Podfile
  ```
  
## 其他的奇淫巧技

1. 偶爾會有compile上得問題，適時的清除derivedData

  ```
  rm -rf ~/Library/Developer/Xcode/DerivedData/*
  ```
  
2. 正確的重新安裝pods

  ```
  rm -rf ~/Library/Caches/CocoaPods
  rm -rf Pods
  rm -rf ~/Library/Developer/Xcode/DerivedData/*
  pod deintegrate
  pod setup
  pod install
  ```
  
3. 更新某個framework
  ```
  修改要更新的framework版本
  執行 pod update [PodName]
  ```
