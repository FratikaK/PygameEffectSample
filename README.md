# Usage  
effect.pyとimgフォルダを自分のpygameのリポジトリに入れる  

Screen_abcを継承したクラスのdisplayメソッドのsuper.update()をする前に、
draw_effect()を記述する  

```python
from effect import *

def display(self):
    SC.screen.fill((0, 128, 0))

    # super().updateをする前にdraw_effectを入れる
    draw_effect()
    super().update(10)
```

### エフェクトを表示させる場合  
effect.pyにある表示したいエフェクトのクラスのインスタンスを  
effect_group().add()で追加する 

例  SPACEを押したときに氷のエフェクトを表示したい
```python
if event.key == K_SPACE:
  effect_group.add(IceEffect(x座標,y座標))

```
