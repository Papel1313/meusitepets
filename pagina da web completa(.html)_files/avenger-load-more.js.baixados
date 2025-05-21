jQuery(document).ready( function($){	
	
	/* Ajax functions */
	$(document).on('click','.avenger-load-more', function(){

		var that = $(this);
		var page = $(this).data('page');
		var newPage = page+1;
		
		var ajaxurl = that.data('url');
		
		var categoria = $(this).data('categoria');
		
		$.ajax({
			
			url : ajaxurl,
			type : 'post',
			data : {
				categoria  : categoria,
				page : page,
				action: 'avenger_load_more'
				
			},
			error : function( response ){
				console.log(response);
			},
			success : function( response ){
				
				that.data('page', newPage);
				that.data('categoria', categoria);
				$('.avenger-posts-container').append( response );
				
			}
			
		});
		
	});
});