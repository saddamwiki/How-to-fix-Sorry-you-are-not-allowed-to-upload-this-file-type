# How to fix ( Sorry, you are not allowed to upload this file type ) Error


# // SVG File Uploads Code

## Site Tools > Site > File Manager >
 
 ## or goto cpanel and file manager then =
 
 ## public_html/wp-includes/functions.php
 ### Then past this code and save


function add_file_types_to_uploads($file_types){
	$new_filetypes = array();
	$new_filetypes['svg'] = 'image/svg+xml';
	$file_types = array_merge($file_types, $new_filetypes );
	return $file_types;
}
add_filter('upload_mimes', 'add_file_types_to_uploads');
