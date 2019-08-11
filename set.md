# __パソコンの各種設定__


## __Docker カスタマイズ__
---
## __Jupyter カスタマイズ__

### ■ __初期ディレクトリの変更__
jupyter notebook --generate-config  
C:\Users\comuser\.jupyter  
##The directory to use for notebooks and kernels.のコメント記号を外す


### ■ __テーマの変更__
__1 ライブラリのインストール__  
pip install jupterthemes

__2 テーマの設定__  
jt -t grade3 -N -fs 10 -ofs 10 -f hack -lineh 130 -tfs 10 -cellw 98%

__3 テーマの修正 (change color and style)__  
__File Dir : C:\Users\username\\.jupyter__  
__Change Color__  
- ffffff ⇒ ededed  
- e5e5e5 ⇒ ffffff  
- .cm-s-ipython.CodeMirror { ⇒ ffffff  
- div.cell.selected .out_prompt_overlay.prompt ⇒ ffffff  
- .btn-default { ⇒ line 928 ⇒ ededed  
- .btn-default { ⇒ line 929 ⇒ 0px  

__h1 h2 h3 h4 h5 インデント設定__  
 - .rendered_html h1  
   font-weight: normal; ⇒ font-weight: 700;  
   #126dce ⇒ #1254ce  
 margin-bottom: 0.3em !important; の下に margin-left: 0em !important; を追加

### __■ 行数を表示する__
- __custom.jsファイルに下記PRGを追加__  
/**  
Display line numbers in code cell by default  
*/  
var cell = Jupyter.notebook.get_selected_cell();  
var config = cell.config;  
var patch = {  
  CodeCell:{  
    cm_config:{lineNumbers:true}  
  }  
}  
config.update{patch}  


---
