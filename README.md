# 0506Hit-the-keys

## 小型打字遊戲

> { 深入淺出C# }  Book Practice!


     表單隨機顯示幾個字元，若玩家TYPE中其中一個，此字元就會消失。
     The form randomly displays a few characters.
     If player answer is correct, the character will disappear!
     正確率上升，遊戲時間便會加快，若表單充滿字元就Game Over!
     As the rate of correct answer increase, time will accelerate.
     If the form is full, the game will over!


### Setting
-   Form :

        1. Min and Max -> False
        
        2. FormBorderStyle -> "Fixed 3D"
            (使玩家不會意外調整到大小)
            
        3. 調整尺寸 Size -> 886, 173
        
        ketpreview -> True
    
-   ListBox : 

        1. Font -> "Microsoft Sans Serif, 72pt, style=Bold"
        2. MultiColumn -> "True"
        3. selectionMode -> None
        3. Dock -> "fill"
    
-   Timer :

        1. private void timer1_Tick Script
    
-   StatusStrip :

        1. SizingGrip -> "False"

        2. + StatusLabel X 4 
               Name) -> (correctLabel、missedLabel、totalLabel、accuracyLabel) 
               Text -> Correct:0、Missed:0、Total:0、Accuracy:0% 
            
        3. + StatusLabel X 1
               Spring -> "True"
               TextAlign -> "MiddleRight"
               Text -> "Difficulty"

        4. + ProgressBar
               (Name) -> difficultyProgressBar

### Stats Class

> 建立新類別紀錄玩家按鍵總次數、按錯、按對、正確率

        1. int Total, Missed, Correct, Accuracy

        2. add a method of Update
            
### Form
        1. Properties Event(閃電圖案) -> KeyDown Double clicked
          (IDE會建立一個Form1_KeyDown的method)
        2. + 檢查輸入的字母是否正確
