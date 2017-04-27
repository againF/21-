# 21-
一个函数，实现21点算法，它根据参数card的值来递增或递减变量count，函数返回一个由当前count和 "Bet"(count>0)或"Hold"(count&lt;=0) 拼接的字符串。
/*
在赌场21点游戏中，玩家可以通过计算牌桌上已经发放的卡牌的高低值来让自己在游戏中保持优势，这就叫21点算法。

根据下面的表格，每张卡牌都分配了一个值。如果卡牌的值大于0，那么玩家应该追加赌注。反之，追加少许赌注甚至不追加赌注。
count change    cards
    +1           2, 3, 4, 5, 6
     0           7, 8, 9
    -1           10, 'J', 'Q', 'K','A'
*/
var count = 0;
function cc(card) {
switch(card) {
  case 2:
  case 3:
  case 4:
  case 5:
  case 6:
     count++;
     break;
  case 10:
  case "J":
  case "Q":
  case "K":
  case "A":
     count--;
     break;
}
if(count > 0){return (count + " Bet");}
  else
return (count + " Hole");
}

//test use case
cc(2); cc(3); cc(7); cc('K'); cc('A');
