# phpstorm_codeigniter_3_auto_complete

to be able auto complete Phpstorm on codeigniter 3 follow these steps 

1- mark your root folder (where index.php is under this folder) as Resource root
2- mark system folder as Sources root
3- inside any model php file if you want to use $this->db  auto complete add this line top of my_example_model.php file 
it must be look like this 

    <?php defined('BASEPATH') OR exit('No direct script access allowed');
    /**
    * @property CI_DB_query_builder $db
    */
    class Db_table_model extends CI_Model
    {
    public function __construct()
    {

        parent::__construct();
        

now phpstorm will autocomplete your db functions.it is recomended restart phpstorm

if you want to also autocomplete model functions you can add like this . in this example i have a model which is apimodel 


    <?php defined('BASEPATH') OR exit('No direct script access allowed');

    /**
    * @property apimodel $apimodel
    * @property CI_DB_query_builder $db
    */
    class Db_table_model extends CI_Model
    {


    public function __construct()
    {

        parent::__construct();
        
        
        
now i can use my apimodel functions like this 

$this->apimodel->gen_new_api($nome);
