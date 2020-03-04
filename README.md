# プログラミング基礎問題 3

## はじめに

Ruby をもちいた基礎プログラミング練習！  
以下の問題にチャレンジしてみてください！  
それぞれ別の ruby ファイルを作ってね

オブジェクト指向の練習問題です！  
各問題で，クラスを定義し，適切にメソッドを定義するなどして実装してください

## 1. 名前

ファイル名： `name.rb`

以下のプログラムで，出力例にあるように出力がされるクラス`User`を定義してください．

プログラム

```ruby:user.rb
amitan = User.new('Ami', 'Shiratori')
amitan.get_first #名を出力
amitan.get_last #姓を出力
amitan.get_full #フルネームを出力
```

出力例

```
Ami
Shiratori
Ami Shiratori
```

## 2.

## 面積計算

ファイル名： `area.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`Circle`, `Rectangle`を定義してください．

プログラム

```ruby:area.rb
shapes = [Circle.new(1.5), Rectangle.new(2, 4)]
shapes.each do |shape|
  puts shape.area # 四角形と円の面積を出力
end
```

出力例

```
7.065
8
```

## 3.

## バリデーション

ファイル名： `user_validation.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`User`を定義してください．

プログラム

```ruby:user_validation.rb
ami = User.new("ami", "ami@sample.com")
kai = User.new("kai", "kaisample.com")

puts ami.has_valid_email
puts kai.has_valid_email
```

出力例

```
true
false
```

## 4.

## 塩水

ファイル名： `salt_water.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`SaltWater`を定義してください．

プログラム

```ruby:salt_water.rb
salt_water = SaltWater.new(90.0, 1.0)
salt_water.add_solute(9.0)  #塩を追加
salt_water.add_solvent(10.0) #水を追加
salt_water.abandon_solution(20.0) #食塩水を捨てる

puts salt_water.strength #濃度を出力
puts salt_water.solute #塩の量を出力
```

出力例

```
10
8
```
