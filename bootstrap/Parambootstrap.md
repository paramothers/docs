# BootStrap 3.1.1

   is a CSS framework, developed in 2011
   
   - BootStrap 1.0 released in 2011 only with CSS and HTML only
   - BootStrap 2.0 released in 2012 and javascript plugin has been introduced for responsive framework.
   - BootStrap 3.0 released in 2013, as mobile first and responsive framework.
   - BootStrap 3 use CSS3, and HTML 5
  
 it uses JQuery
 it introduce some of Meta attrubite

other CSS framework are

 1. YUI ( Yahoo User Interface library )
 2. BluePrint

Above are used just CSS. 
But BootStrap has added JavaScript with CSS and understand HTML tags

# Responsive
   it means, the layout of the page can changed on the go. so the desing will work in any size of devices.
   

grep -rl 'src="' ./ | xargs sed -i 's/src="/linux/g' *.html
grep -rl 'linux' ./ | xargs sed -i 's/linux/src="\/deploy\/asset\/img\//g' *.html