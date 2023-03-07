# Word, Character and Paragraph Counter :computer:
##### This PHP application counts the number of words, characters, and paragraphs in the entered text.

##     How to Use?
```
     1.Run the index.php file on a PHP server.
     2.Enter your text in the textarea.
     3.Click the "Submit" button.
     4.The results will be displayed below.
 ```
 ##     Code Examples
 
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
+ This code is a sample code.
