#RubyGold試験対策　ソースコード及び実行結果

#実行環境
##コマンドラインオプション
###-w
ソースコード

	class Foo 
		attr_accessor :bar
	#@barは初期化されていないため、funcを実行すると
	#nilが表示される。しかし、このnilは明示的に代入
	#した値ではない。
	#-wオプションをつけて実行すると、@barが初期化さ
	#れていないことを表示する
		def func
			puts @bar
		end
	end
	f = Foo.new
	f.func

実行結果

	M:\prog\waraya\RubyGold\V01\sample>ruby warning.rb
	nil

	M:\prog\waraya\RubyGold\V01\sample>ruby -w warning.rb
	warning.rb:9: warning: instance variable @bar not initialized

	nil
