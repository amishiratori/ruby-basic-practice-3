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
patty = User.new("patty", "fatty_patty@sample.com")
bob = User.new("bob", "robert.armstrong.com")

puts patty.has_valid_email
puts bob.has_valid_email
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
salt_water.add_solute(9.0)          # 塩を追加
salt_water.add_solvent(10.0)        # 水を追加
salt_water.abandon_solution(20.0)   # 食塩水を捨てる

puts salt_water.strength            # 濃度を出力
puts salt_water.solute              # 塩の量を出力
```

出力例

```
10
8
```

## 5.

## RPG

ファイル名： `rpg.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`Player, Enemy`を定義してください．

プログラム

```ruby:rpg.rb
regina = Player.new("Regina", 1000, 30) # 名前, 体力, 攻撃力で初期化
slime = Enemy.new("slime", 300, 10)    # 同じく初期化
regina.attack(slime)          # 攻撃
regina.gain_power(300)         # 攻撃力を上昇
regina.attack(slime)          # 攻撃
```

出力例

```
Reginaのslimeへの攻撃 30ダメージ
Reginaは攻撃力が300上昇した
Reginaのslimeへの攻撃 330ダメージ
slimeは死亡した
```

## 6.

## RPG2

ファイル名： `rpg2.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`Player`を定義してください．

プログラム

```ruby:salt_water.rb
dixie = Player.new("dixie", 100, 0, 0) # 名前, 体力, 座標で初期化
dixie.move_east(40)                 # 移動
dixie.move_south(50)                # 移動
puts dixie.is_hungry                 # 体力が一定以下になるとhungry状態になる
```

出力例

```
dixieの現在の座標: 40, 0 体力が40減った
dixieの現在の座標: 40, -50 体力が50減った
true
```

## 7.

## ピラミッドドロワー

ファイル名： `pyramid_drawer.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`PyramidDrawer`を定義してください．

プログラム

```ruby:pyramid_drawer.rb
drawer = PyramidDrawer.new(5) # 高さで初期化
drawer.execute                # 描画
drawer.set_height(3)          # 高さ更新
drawer.execute
```

出力例

```
    *
   ***
  *****
 *******
*********
  *
 ***
*****
```

## 8.

## じゃんけん

ファイル名： `janken.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`Player, Referee`を定義してください．

プログラム

```ruby:janken.rb
# Player.new(名前, ぐーの確率, ちょきの確率, ぱーの確率)
magnolia = Player.new("magnolia", 1, 1, 1)
patty = Player.new("patty",2, 1, 0,)       # 同じく初期化
stela = Referee.new("Stela Rose")                      # 審判クラスを初期化
stela.judge(patty, magnolia)               #試合を行う
```

出力例 (どちらが勝つかはランダム)

```
patty win
```

## 9.

## ガチャ

ファイル名： `gacha.rb`
以下のプログラムで，出力例にあるように出力がされるクラス`Monster, Gacha`を定義してください．

プログラム

```ruby:gacha.rb
gacha = Gacha.new                 # ガチャを初期化
monster = Monster.new('Slime', 6) # 名前とオッズで初期化
gacha.add_monster(monster)
gacha.add_monster(Monster.new('Fogghoul', 5))
gacha.add_monster(Monster.new('Wispfang', 4))
gacha.add_monster(Monster.new('Venomwraith', 2))
gacha.add_monster(Monster.new('The Cobalt Frost Ape', 3))
gacha.add_monster(Monster.new('Vaporman', 4))
gacha.add_monster(Monster.new('The Feral Hunting Gorrila', 1))
puts gacha.odds('Fogghoul')  # オッズを取得
gacha.draw
```

出力例 (何が出るかははランダム)

```
0.2
you get Vaporman
```
