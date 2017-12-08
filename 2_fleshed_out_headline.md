### lambdaについて
Rubyにおいてブロックはオブジェクトではありません。
つまり、文字列や数字や配列などの他のオブジェクトとは異なり、Rubyではそれを直接
変数に代入したり、他の関数に渡したりすることはできません。
しかし「lambda」を使うことで、ブロックとして書いた手続きそのものを
Procオブジェクトとすることができます。

※ブロックはdo ... endまたは{ ... }で囲まれた手続きのかたまりです。

例を示します。ファイル名はlambda.rbです。

>>> square = lambda{ |n| n*n }  
>>> square.call(3)
>>> 
>>> def print_func(arg,fun)    
>>>	 puts  fun.call(arg)  
>>> end
>>>
>>> print_func(4,square)

実行結果
$ ruby lambda.rb  
9  
16

以上の例では、インスタンス変数squareにProcオブジェクトを代入し、
callメソッドによりlambdaで定義したProcオブジェクトを呼び出しています。
callメソッドに与えた引数が、そのままブロック引数に対応します。  
また、print_funcというメソッドに引数としてProcオブジェクトを与えています。