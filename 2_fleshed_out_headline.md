### lambdaについて
Rubyにおいてブロックはオブジェクトではありません。
つまり、文字列や数字や配列などの他のオブジェクトとは異なり、Rubyではそれを直接
変数に代入したり、他の関数に渡したりすることはできません。
しかし「lambda」を使うことで、ブロックとして書いた手続きそのものを
Procオブジェクトとすることができます。

例としてlambda.rbを示します。

square = lambda{ |n| n*n }

square.call(3)

def print_func(arg,fun)
  puts  fun.call(arg)
end

print_func(4,square)


lambda.rbの実行結果

$ruby lambda.rb
9
16


このようにブロックをProcオブジェクトでラップすれば、
変数に代入したり、メソッドに引数として渡したりすることが
できるようになります。
