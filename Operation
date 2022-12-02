<?php
class Operation
{
    public function get_addition($nb1, $nb2)
    {
        return $nb1 + $nb2;
    }
    public function get_minus($nb1, $nb2)
    {
        return $nb1 - $nb2;
    }
    public function get_multiplication($nb1, $nb2){
        return $nb1 * $nb2 ;
    }
    public function get_division($nb1, $nb2)
    {
        return $nb1 / $nb2 ;
    }
}
?>
<html>
    <body>
    <form method="post">
        <p>Please type + for Addition, - for Minus, x for Multiplication and / for Division</p>
        <p> Operation: <input name="operation" type="text"></p>
        <p>Operand 1: <input name="nb1" type="text"></p>
        <p>Operand 2: <input name="nb2" type="text"></p>
        <button name="form_action" type="submit" value="Validate"> Validate </button>
        <p> Result:
            <?php
            try {
                $operation = new Operation;
                if(isset($_POST['form_action']))
                {
                    if($_POST['operation'] == '+'){
                        echo $operation->get_addition($_POST['nb1'], $_POST['nb2']);
                    }elseif($_POST['operation'] == '-'){
                        echo $operation->get_minus($_POST['nb1'], $_POST['nb2']);
                    }elseif ($_POST['operation'] == 'x'){
                        echo $operation->get_multiplication($_POST['nb1'], $_POST['nb2']);
                    }elseif ($_POST['operation'] == '/'){
                        if($_POST['nb2'] == 0){
                            echo 'Operand 2 Must not be 0';
                        }else{
                            echo $operation->get_division($_POST['nb1'], $_POST['nb2']);
                        }
                    }else{
                        echo 'Invalid operation! Please type + for Addition, - for Minus, x for Multiplication and / for Division';
                    }
                }
            }catch (Exception $exception){
                return $exception->getMessage();
            }
            ?>
        </p>
        </form>
    </body>
</html>


