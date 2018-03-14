# edd-trusted-reviews
Add support for Trusted Reviews to Easy Digital Downloads

## Step 1
Go to wp-content/plugins/easy-digital-downloads/templates/shortcode-reciept.php

## Step 2
Add the following code to the very bottom of your shortcode-reciept.php file (even below the <?php endif; ?> tag):

<script src="https://cdn.trustedsite.com/js/conversion.js"
  class="trustedsite-track-conversion"
  data-type="purchase"
  data-orderid="<?php echo edd_get_payment_number( $payment->ID ); ?>"
  data-email="<?php echo edd_get_payment_user_email( $payment->ID ); ?>"
  data-country="US"
  ></script>
  
## Step 3
Enjoy
