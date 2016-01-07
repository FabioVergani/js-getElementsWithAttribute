# js-getElementsWithAttribute
getElementsWithAttribute

 var getElementsWithAttribute=(function(aDoc){
	var d=aDoc;
	return d.querySelectorAll ? function(s){
		return s===''?[]:Slice(d.querySelectorAll('['+s+']'));
	}:function(s){
	 var e,h=d.getElementsByTagName('*'),i=h.length+0,m=[];
	 while((e=h[--i])!==undefined){
		if(e.hasAttribute(s)){m[m.length]=e;};
	 };
	 return m;
	};
 })(w.document);
