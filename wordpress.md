# Media upload
```
<?php wp_enqueue_media(); ?>

<span id="show-image">
<?php if($imageU){ echo '<img src="'.$imageU.'" style="height:100px;width:100px">'; }else{ } ?>
</span><br>
<input type="hidden" id="image_name" value="<?php echo $imageU; ?>" name="image_name"/>
<input type="button" value="Upload Image" class="button btn btn-info" id="upload_image_button"   />
 
 
<script type='text/javascript'>
	jQuery( document ).ready( function( $ ) {
		jQuery("#upload_image_button").on("click", function() {
		var image = wp.media({
		    title: "Upload Image for data center",
		    mulitple: false
		}).open().on("select", function() {
		    var uploaded_image = image.state().get("selection").first();
		    var getImage = uploaded_image.toJSON().url;
		    jQuery("#show-image").html("<img src='" + getImage + "' style='height:100px;width:100px'/>")
		    jQuery("#image_name").val(getImage);
		});
	    });
		jQuery(function() {
		    jQuery('.multiselect-ui').multiselect({
			includeSelectAllOption: true
		    });
		});

	});
</script>
  
  
