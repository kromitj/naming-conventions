#Naming Conventions

##Ruby Naming Convention

*Ruby uses the first character of the name to help it determine it’s intended use.*
<dl>
	<dt>**Local Variables**</dt>
	<dd>Lowercase letter followed by other characters, naming convention states 	that it is better to use underscores rather than camelBack for multiple word 	names, *e.g. mileage, variable_xyz*</dd>
	<dt>**Instance Variables**</dt>	
	<dd>Instance variables are defined using the single "at" sign (@) followed 	by a name. It is suggested that a lowercase letter should be used after the 	@, *e.g. @colou*r</dd>
	<dt>**Instance Methods**</dt>
	<dd>Method names should start with a lowercase letter, and may be followed 	by digits, underscores, and letters, *e.g. paint, close_the_door*</dd>
	<dt>**Class Variable**s</dt>
	<dd>Class variable names start with a double "at" sign (@@) and may be 	followed by digits, underscores, and letters, *e.g. @@colour*</dd>
	<dt>**Constant**</dt>
	<dd>Constant names start with an uppercase letter followed by other 	characters. Constant objects are by convention named using all uppercase 	letters and underscores between words, *e.g. THIS_IS_A_CONSTANT*</dd>
	<dt>**Class and Modul**e</dt>
	<dd>Class and module names starts with an uppercase letter, by convention 	they are named using MixedCase, *e.g. module Encryption, class MixedCase*</dd>
	<dt>**Global Variable**s</dt>
	<dd>Starts with a dollar ($) sign followed by other characters, *e.g. 	$global*</dd>
<dl>

##Rails Naming Convention

*Rails use the same naming convention as Ruby with some additions:*
<dl>
	<dt>**Variable**</dt>
	<dd>Variables are named where all letters are lowercase and words are 	separated by underscores, *e.g. order_amount, total*</dd>
		<dt>**Class and Module** </dt>
		<dd>Classes and modules use MixedCase and have no underscores, each word 		starts with a uppercase letter, *e.g. InvoiceIte*m</dd>
		<dt>**Database Table**</dt>
		<dd>Table names have all lowercase letters and underscores between 		words, also all table names need to be plural, *e.g. invoice_items, 		orders*</dd>
		<dt>**Model** </dt>
		<dd>The model is named using the class naming convention of unbroken 		MixedCase and is always the singular of the table name, *e.g. table name 		might be orders, the model name would be Order. Rails will then look for 		the class definition in a file called order.rb in the /app/models 		directory. If the model class name has multiple capitalised words, the 		table name is assumed to have underscores between these words.*</dd>
		<dt>**Controller**</dt>
		<dd>Controller class names are pluralized, such that OrdersController 		would be the controller class for the orders table.  Rails will then 		look for the class definition in a file called orders_controller.rb in 		the /app/	controllers directory.</dd>
		<dt>**Files, Directories and other pluralization**</dt>
		<dd>
		Files are named using lowercase and underscores. Assuming we have an 		Orders controller then the following other conventions will apply:
		<ul>
			<li>Rails will look for view template files for the controller in 			the app/views/orders directory</li>
			<li>Output from this view will then be used in the layout defined in 			the orders.html.erb in the app/views/layouts directory</li>
			<li>Test files including order_test.rb will be created in the /test/			unit directory, a file will be created in the /test/fixtures 			directory called orders.yml and finally a file called 			orders_controller_test.rb will be created in the /test/functional 			directory</li>
		</ul>
		<dt>**Primary Key**</dt>
		<dd>The primary key of a table is assumed to be named id.</dd>
		<dt>**Foreign Key**</dt>
		<dd>The foreign key is named with the singular version of the target 		table name with _id appended to it, *e.g. order_id in the items table 		where we have items linked to the orders table.*</dd>
		<dt>**Many to Many Link Tables**</dt>
		<dd>Tables used to join two tables in a many to many relationship is 		named using the table names they link, with the table names in 		alphabetical order, for example items_orders.</dd>
		<dt>**Automated Record Timestamps**</dt>
		<dd>You can get ActiveRecord to automatically update the create and 		update times of records in a database table. To do this create two 		specially named columns created_at and updated_at to your table, *i.e. 		t.datetime :created_at and t.datetime :updated_at. If you only want to 		store the date rather than a date and time, use :created_on 		and :updated_on.*</dd>
	</dl>

##Naming Convention Summary 

###Model Naming Convention
<table style="width:100%">
  	<tr><td>Table:</td><td>orders</td></tr>
  	</tr><tr><td>Class:</td> <td>Order</td></tr>
	<tr><td>File:</td> <td>/app/models/order.rb</td></tr>
	<tr><td>Primary Key:</td> <td>id</td></tr>
	<tr><td>Foreign Key:</td> <td>customer_id</td></tr>
	<tr><td>Link Tables:</td> <td>items_orders</td></tr>  
</table>

###Controller Naming Convention
<table style="width:100%">
	<tr><td>Class:</td><td>OrdersController</td></tr>
	<tr><td>File:</td><td>/app/controllers/orders_controller.rb</td></tr>
	<tr><td>Layout:</td><td>/app/layouts/orders.html.erb</td></tr>
</table>
###View Naming Convention
<table style="width:100%">
<tr><td>Helper:</td> <td>/app/helpers/orders_helper.rb<td></tr>
<tr><td>Helper Module:</td> <td>OrdersHelper<td></tr>
<tr><td>Views:</td> <td>/app/views/orders/… (list.html.erb for example)<td></tr>
</table>
###Tests Naming Convention
<table style="width:100%">
<tr><td>Unit:</td> <td>/test/unit/order_test.rb</td><tr>
<tr><td>Functional:</td> <td>/test/functional/orders_controller_test.rb</td><tr>
<tr><td>Fixtures:</td> <td>/test/fixtures/orders.yml</td><tr>
</table>