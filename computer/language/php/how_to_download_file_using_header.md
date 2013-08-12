# header를 이용해서 file download하기

    <?php
    $file_name = "sample.txt";
    header('Pragma: public');
    header('Expires: 0');
    header('Cache-Control: must-revalidate, post-check=0, pre-check=0');
    header('Cache-Control: private',false);
    header('Content-Type: application/force-download');
    header('Content-Disposition: attachment; filename="'.basename($file_name).'"');
    header('Connection: close');
    readfile($file_name);
    ?>
