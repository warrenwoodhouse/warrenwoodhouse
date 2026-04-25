```
/*
Different Backgrounds After Clock Times
Author: Warren Woodhouse warrenwoodhouse.blogspot.com/codes
*/

<script language="JavaScript">

<!-- Hide From Old Browsers

/* ?2010-2016 JavaScript written by Warren Woodhouse @ www.warrenwoodhouse.blogspot.com --- This simple script changes the background image four times a day -- It can be altered to include other page attributes such as text colours and individual page items such as on the example page - Use freely but keep this entire credit line intact. */

day=new Date()     //..get the date

x=day.getHours()    //..get the hour

if(x>=0 && x<4) {

   document.write('<body background="put your first image file name here such as 1.jpg">')

} else

if(x>=4 && x<12) {

   document.write('<body background="put your second image file name here such as 2.jpg">')

} else

if(x>=12 && x<18) {

   document.write('<body background="put your third image file name here such as 3.jpg">')

} else

if (x>=18 && x<24) {

   document.write('<body background="put your last image file name here such as 4.jpg">')

}

<!-- End Hiding -->

</script>
```
