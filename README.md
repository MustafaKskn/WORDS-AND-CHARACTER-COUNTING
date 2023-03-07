# Word, Character and Paragraph Counter :computer:
>This PHP application counts the number of words, characters, and paragraphs in the entered text.
</br>

>##     How to Use?
```
     1.Run the kelimesayac.php file on a PHP server.
     2.Enter your text in the textarea.
     3.Click the "Submit" button.
     4.The results will be displayed below.
 ```
 ##     Code Examples :memo:

 
 ```
 <!DOCTYPE html>
<html>
<head>
	<title>Word, Character, and Paragraph Counter</title>
</head>
<body>
	<form method="post">
		<textarea name="text"></textarea><br>
		<input type="submit" name="submit" value="Submit"><br><br>

		<?php
		if(isset($_POST['submit'])){
			$text = $_POST['text'];

			// Count the number of words
			$word_count = str_word_count($text);

			// Count the number of characters
			$clean_text = str_replace(" ", "", $text);
			$char_count = strlen($clean_text);

			// Count the number of paragraphs
			$paragraph_count = preg_match_all('/\n/', $text) + 1;

			echo "The text contains $word_count words, $char_count characters, and $paragraph_count paragraphs.";
               
		}
		?>
	</form>
</body>
</html>
```

>###### This code is a sample code. :warning:
</br>

> ###### The above code is located in the index.php file and calculates the number of words, characters, and paragraphs in the given text. The text is entered in the textarea and submitted by clicking the "Submit" button. The results are displayed at the bottom of the page.
</br>

>## Resources

+ The following PHP functions were used in this application:
+ str_word_count(): Returns the number of words in a specified string.
+ str_replace(): Replaces all occurrences of the search string with the replacement string.
+ strlen(): Returns the length of a string.
+ preg_split(): The preg_split() function splits a string into an array of substrings based on a specified regular expression pattern.

</br>

 >## The output of the code :printer:
 
 <a><img src="https://github.com/MustafaKskn/WORDS-AND-CHARACTER-COUNTING/blob/aace22185e4ff1f1679b72cb5455bba135a6631a/kelimesayac/imges/Ekran%20Al%C4%B1nt%C4%B1s%C4%B1.PNG">
<img src="https://github.com/MustafaKskn/WORDS-AND-CHARACTER-COUNTING/blob/ec97a6cec604a0fd32a01334858b2d16e95d833e/kelimesayac/imges/Ekran%20Al%C4%B1nt%C4%B1s%C4%B12.PNG"></a>
