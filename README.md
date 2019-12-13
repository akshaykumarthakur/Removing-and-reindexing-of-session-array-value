# Removing-and-reindexing-of-session-array-value
Removing the specific value from the session array and re indexing  the session array in PHP codeigniter.

#Removing the value

    unset($_SESSION['array_name']['sub_array'][sub_array_key]);

#reindexing the session array
  //function call

    $this->reindex($_SESSION['array_name']['sub_array']);
    
  //function defination
  
    function reindex(&$the_array) {
        $temp = $the_array;
        $the_array = array();
        foreach($temp as $value) {
          $the_array[] = $value; 
        } 
      }
