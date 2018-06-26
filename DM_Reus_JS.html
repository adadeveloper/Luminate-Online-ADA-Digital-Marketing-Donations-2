var jQDM = jQuery.noConflict(true);
var ie = getInternetExplorerVersion();
var currDMDFID;
var whatIsToday = new Date();
var startWidth;

jQDM(document).ready(function(){
	DFHandler();
});

function DFHandler(){
	startWidth = jQDM(window).width();
	
	//grab the DFID from the hidden input
	if(window.location.href.indexOf("donation=completed") > -1) {
		currDMDFID = getURLParameter("df_id");
		//hide right col and stretch ty page
		jQDM('#dmcontentR').hide();
		jQDM('#dmcontentL').css({'max-width':'800px','width':'100%','float':'none','margin':'0 auto'});
		jQDM('div.responsive').css('max-width','800px');
	} else if(getURLParameter("df_id")!="null"){
		currDMDFID = getURLParameter("df_id");
	} else{
		currDMDFID = jQDM('#df_id').val();
	}
	
	if (window.console) {
		console.log("DFID: "+currDMDFID);
		console.log("DFIDparam: "+getURLParameter("df_id"));		
	}	
	//copyright year update
	jQDM('#copyThisYear').text(whatIsToday.getFullYear());
	
	//Look for checked radio button to create pre-selected button on pageload
	jQDM('div.donation-level-label-input-container input[checked="checked"]').closest('.donation-level-input-container').find('.donation-level-label-container').addClass('active');

	//Add active class to selected donation level (button)
	jQDM('.donation-level-amount-container, .donation-level-label-container').click(function() {
	   if(jQDM(this).closest('.donation-level-label-input-container input[type="radio"]').attr('checked', 'checked')) { 
		  jQDM('div.donation-level-input-container .active').removeClass('active');   
		  jQDM(this).addClass('active'); 
	   }
	});

	//Add active class to corresponding 'Other' button on input focus
	jQDM('.donation-level-user-entered input[type="text"]').focus(function(){
	  jQDM('div.active').removeClass('active');
	  jQDM(this).parent('div.donation-level-user-entered').siblings('label').children('.donation-level-label-container').addClass('active');
	});
	
	//memorial / honor occasion preset
	/*if(jQDM('#occasion_dropdown').length){ 
		//jQDM('#occasion_dropdown').val(jQDM('#occasion_dropdown option:first').val());
		jQDM('#occasion_dropdown option:first').prop('selected','selected');
		//console.log(jQDM('#occasion_dropdown').val())
	}*/
		
	if(ie == 8){
		jQDM('.donation-level-container:eq(6)').css({'width':'250px'});
	}
	
	if((ie != 8)&&(ie != 9)){
		doPlaceHolder();
	}
	
	//add dollar sign on user entered donation text
	jQDM('.donation-level-user-entered').prepend('<span class="dollarSign">$</span>&nbsp;');
	
	//take off the first border top on df header section
	if(jQDM('.form-message-text').length){
		jQDM('.section-header-container:eq(0)').css({'border-top':'1px solid','padding-top':'20px'});
	} else {
		jQDM('.section-header-container:eq(0)').css({'border-top':'none','padding-top':'0'});
	}
	
	//regroup into tab
	regroupAskLvl();
	
	//add ID on cvv link class
	jQDM('.HelpLink:eq(0)').prop('id','whatcvvori');
	jQDM('#whatcvvori').hide();
	jQDM('<a href="javascript:void(0);" id="whatcvv">What\'s CVV?</a>').insertAfter(jQDM('#whatcvvori'));
	jQDM('#whatcvv').on('click', function(){
		jQDM.magnificPopup.open({
		  items: {
			  src: '#cvvpop',
			  type: 'inline'
		  }      
  		});
	});
	magnificPopupsHandler();
	
	//Gift Notification Handler
	if(jQDM('#gift_information_input').length){
		if (window.console) {		
			console.log("Notification Component Exist");
		}
		if((ie != 8)&&(ie != 9)){
			jQDM('<span id="lblTo">To : </span>').insertBefore(jQDM('#recipient_name_s__input'));
			jQDM('<span id="lblFrom">From : </span>').insertBefore(jQDM('#tribute_signaturename'));
		}
		giftNotifHandler();
	}
	
	//if progress label exist
	if(jQDM('.progress-bar-step-container').length){
		var pbarlaststepnum = jQDM('.progress-bar-step-container').length + 1;
		var pblastindex = jQDM('.progress-bar-step-container').length - 1;
		jQDM('<div class="progress-bar-step-container"><div class="progress-bar-step-number-container">'+pbarlaststepnum+'</div><div class="progress-bar-step-text-container">Thank you</div></div>').insertAfter(jQDM('.progress-bar-step-container:eq('+pblastindex+')'));
	}
	
	//if tribute type exist
	if(jQDM('#tribute_type').length){
		jQDM('#tribute_type option:eq('+jQDM.trim(jQDM('#preselect_occasion_val').text())+')').prop('selected','selected');
	}
	
	//renderRightCol donation specific
	renderRightCol(currDMDFID);
	
	//screenWidth Resize Handler
	screenWidthHandler();
	
	//validation custom
	jQDM('#ProcessForm').on('submit', function(){
		return cstmFormValidation();
	});
}

function giftNotifHandler(){
	
	var currNotifSelection;
	
	jQDM('#gift_information_input').closest('.custom-field-container').hide();
	
	resetAllNotifDetails();
	
	if (jQDM.trim(jQDM('#gift_information_input').val()) === 'ecard'){	
		currNotifSelection = 1;	
		showECARDDetails();
		jQDM('#giftNotifOpt option:eq(1)').prop('selected','selected');
		if(jQDM('.form-error').length){
				jQDM('.form-error').hide();
				onlyShowECARDError();
		}
		
		
	} else if (jQDM.trim(jQDM('#gift_information_input').val()) === 'printcard'){
		currNotifSelection = 2;
		showPrintCardDetails();
		jQDM('#giftNotifOpt option:eq(2)').prop('selected','selected');
		if(jQDM('.form-error').length){
				jQDM('.form-error').hide();
				onlyShowPrintCardError();
		}	
	} else {
		currNotifSelection = 0;
		jQDM('#giftNotifOpt option:eq(0)').prop('selected','selected');
		//jQDM('#gift_information_input').text('none');
		jQDM('#gift_information_input').val('none');
		if(jQDM('.form-error').length){
				jQDM('.form-error').hide();
		}
	}
	
	jQDM('#giftNotifOpt').change(function(){
		
		//check if this is returned form to warn people if they switch the notification option from previously selected, their populated data might get reset 
		if(getURLParameter("df_id") === "null"){
			if (confirm("Selecting another Gift Notification option might reset your previously selected option and your pre-populated field(s) associated to that option. Do you still want to proceed?") === true) {
				processNotifSelection();
			} else {
				jQDM('#giftNotifOpt option:eq('+currNotifSelection+')').prop('selected','selected');				
			}
		} else {
				processNotifSelection();
		}		
	});
	
	
	var radioECButtons = jQDM("#ProcessForm input:radio[name='stationery_layout_id']");
	var selectedECIndex = radioECButtons.index(radioECButtons.filter(':checked'));
	jQDM('.layout-choice-thumbnail-container').removeClass('activeeCard');
	jQDM('.layout-choice-thumbnail-container:eq('+selectedECIndex+')').addClass('activeeCard');
	
	jQDM('.layout-choice-thumbnail-container').click(function(){
		jQDM('.layout-choice-thumbnail-container').removeClass('activeeCard');
		jQDM(this).addClass('activeeCard');
		jQDM(this).find("input:radio[name='stationery_layout_id']").prop('checked','checked');
	});
}

function processNotifSelection(){
	var selectedNotif = "";
			jQDM('#giftNotifOpt option:selected').each(function(){
				selectedNotif = jQDM.trim(jQDM(this).val());			
			});
			resetAllNotifDetails();
			switch(selectedNotif){
					case "0":				
						//jQDM('#gift_information_input').text('none');
						jQDM('#gift_information_input').val('none');
						if(jQDM('.form-error').length){
							jQDM('.form-error').hide();
						}
					break;
					case "1":				
						//jQDM('#gift_information_input').text('ecard');
						jQDM('#gift_information_input').val('ecard');				
						showECARDDetails();
						if(jQDM('.form-error').length){
							jQDM('.form-error').hide();
							onlyShowECARDError();
						}				
					break;
					case "2":				
						//jQDM('#gift_information_input').text('printcard');	
						jQDM('#gift_information_input').val('printcard');
						showPrintCardDetails();	
						if(jQDM('.form-error').length){
							jQDM('.form-error').hide();
							onlyShowPrintCardError();
						}				
					break;	
			}
}

function onlyShowECARDError(){
	if(jQDM('#ecard_recpients_row').hasClass('form-error')){
		jQDM('#ecard_recpients_row').show();				
	}
	if(jQDM('#tribute_ecard_subject_row').hasClass('form-error')){
		jQDM('#tribute_ecard_subject_row').show();				
	}
	if(jQDM('#tribute_ecard_message_row').hasClass('form-error')){
		jQDM('#tribute_ecard_message_row').show();				
	}
}

function onlyShowPrintCardError(){
	if(jQDM('#tribute_notify_recip_name_row').hasClass('form-error')){
		jQDM('#tribute_notify_recip_name_row').show();				
	}
	if(jQDM('#tribute_notify_recip_street1_row').hasClass('form-error')){
		jQDM('#tribute_notify_recip_street1_row').show();				
	}
	if(jQDM('#tribute_notify_recip_city_row').hasClass('form-error')){
		jQDM('#tribute_notify_recip_city_row').show();				
	}				
	if(jQDM('#tribute_notify_recip_zip_row').hasClass('form-error')){
		jQDM('#tribute_notify_recip_zip_row').show();				
	}
	if(jQDM('.custom-field-container').hasClass('form-error')){
		jQDM('.custom-field-container').show();				
	}
	//exception
	jQDM('#tribute_ecard_message_row').show();
}

function resetAllNotifDetails(){
	resetECardPrintCardValue();
	jQDM('#optNoteDesc').text('');
	jQDM('#giftNotifHeading').text('');
	jQDM('#giftNotifHeading').hide();
	jQDM('#send_ecardname').prop('checked',false);
	jQDM('#send_ecard_row').hide();
	jQDM('#ecard_recpients_row').hide();
	jQDM('#tribute_ecard_subject_row').hide();
	jQDM('#tribute_ecard_message_row').hide();
	jQDM('#select_grid_row').hide();
	jQDM('#ecard_send_date_row').hide();
	jQDM('#e_card_copy_sender_row').hide();
	jQDM('#preview_button_row').hide();
	jQDM('#tribute_notify_recip_street1name').hide();
	jQDM('#tribute_notify_recip_street2name').hide();	
	jQDM('#tribute_notify_recip_cityname').hide();
	jQDM('#tribute_notify_recip_state').hide();
	jQDM('#tribute_notify_recip_zipname').hide();
	jQDM('#tribute_notify_recip_country').hide();
	jQDM('#printSubHeading2').hide();
	jQDM('#recipient_name_s__input').hide();
	jQDM('#memorial-recipient_first_name_input').hide();
	jQDM('#memorial-recipient_last_name_input').hide();
	jQDM('#tribute_signaturename').hide();
	jQDM('#tribute_signaturename').closest('.custom-field-container').hide();
	jQDM('#tribute_signaturename').closest('.form-content').css('margin-top','0');
	jQDM('#tribute_signaturename').closest('.custom-field-container.form-row').css('width','150px');
	if((ie != 8)&&(ie != 9)){
		jQDM('#lblTo').hide();
		jQDM('#lblFrom').hide();
	}
	if((ie == 8)||(ie == 9)){
		//hide labels uncovered by default		
		jQDM("#tribute_notify_recip_name_row").hide();
		jQDM("#memorial-recipient_first_name_input").closest(".form-content").hide();
		jQDM("#memorial-recipient_last_name_input").closest(".form-content").hide();
		jQDM("#tribute_notify_recip_street1_row").hide();
		jQDM("#tribute_notify_recip_street2_row").hide();
		jQDM("#tribute_notify_recip_city_row").hide();
		jQDM("#tribute_notify_recip_state_row").hide();
		jQDM("#tribute_notify_recip_zip_row").hide();
		jQDM("#tribute_notify_recip_country_row").hide();
	}
}
function resetECardPrintCardValue(){
	//restore back to placeholder if they have NA value that comes from submission
	if(jQDM('#gift_information_input').length){		
			
			if(jQDM.trim(jQDM('#recipient_name_s__input').val()) === 'N/A'){	
				jQDM('#recipient_name_s__input').val('');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_first_name_input').val()) === 'N/A'){
				jQDM('#memorial-recipient_first_name_input').val('');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_last_name_input').val()) === 'N/A'){
				jQDM('#memorial-recipient_last_name_input').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_street1name').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_street1name').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_cityname').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_cityname').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_zipname').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_zipname').val('');
			}				
		
			if(jQDM.trim(jQDM('#recipient_name_s__input').val()) === 'N/A'){
				jQDM('#recipient_name_s__input').val('');
			}
			if(jQDM.trim(jQDM('#tribute_ecard_messagename').val()) === 'N/A'){
				jQDM('#tribute_ecard_messagename').val('');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_first_name_input').val()) === 'N/A'){
				jQDM('#memorial-recipient_first_name_input').val('');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_last_name_input').val()) === 'N/A'){
				jQDM('#memorial-recipient_last_name_input').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_street1name').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_street1name').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_cityname').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_cityname').val('');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_zipname').val()) === 'N/A'){
				jQDM('#tribute_notify_recip_zipname').val('');
			}	
	}
}
function showECARDDetails(){
	jQDM('#optNoteDesc').text('eCard can be send now or scheduled for a future date');
	jQDM('#giftNotifHeading').text('eCard Recipient Information');
	jQDM('#giftNotifHeading').show();
	jQDM('#send_ecardname').prop('checked',true);
	jQDM('#send_ecard_row').hide();
	jQDM('#ecard_recpients_row').show();
	jQDM('#tribute_ecard_subject_row').show();
	jQDM('#tribute_ecard_message_row').show();
	jQDM('#select_grid_row').show();
	jQDM('#ecard_send_date_row').show();
	jQDM('#e_card_copy_sender_row').show();
	jQDM('#preview_button_row').show();	
}
function showPrintCardDetails(){
	jQDM('#optNoteDesc').text('Printed cards will be sent within approximately 3-4 business days from your processed donation.');
	jQDM('#giftNotifHeading').text('Card Recipient Information');
	jQDM('#recipient_name_s__input').show();
	jQDM('#memorial-recipient_first_name_input').show();
	jQDM('#memorial-recipient_last_name_input').show();
	jQDM('#tribute_ecard_message_row').show();
	jQDM('#tribute_notify_recip_street1name').show();
	jQDM('#tribute_notify_recip_street2name').show();	
	jQDM('#tribute_notify_recip_cityname').show();
	jQDM('#tribute_notify_recip_state').show();
	jQDM('#tribute_notify_recip_zipname').show();
	jQDM('#tribute_notify_recip_country').show();
	jQDM('#printSubHeading2').show();
	jQDM('#tribute_signaturename').show();
	jQDM('#tribute_signaturename').closest('.custom-field-container').show();
	jQDM('#tribute_signaturename').closest('.form-content').css('margin-top','-15px');
	jQDM('#tribute_signaturename').closest('.custom-field-container.form-row').css('width','300px');
	if((ie != 8)&&(ie != 9)){
		jQDM('#lblTo').show();
		jQDM('#lblFrom').show();		
	}
	if((ie == 8)||(ie == 9)){		
		//show labels uncovered by default		
		jQDM("#tribute_notify_recip_name_row").show();
		jQDM("#memorial-recipient_first_name_input").closest(".form-content").show();
		jQDM("#memorial-recipient_last_name_input").closest(".form-content").show();
		jQDM("#tribute_notify_recip_street1_row").show();
		jQDM("#tribute_notify_recip_street2_row").show();
		jQDM("#tribute_notify_recip_city_row").show();
		jQDM("#tribute_notify_recip_state_row").show();
		jQDM("#tribute_notify_recip_zip_row").show();
		jQDM("#tribute_notify_recip_country_row").show();	
	}
}

function screenWidthHandler(){
	if (jQDM(window).width() > 999) {
      if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
		 jQDM('#dmcontentR').insertAfter(jQDM('#dmcontentL'));
	  }	 
    } else {		  			
      if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
		 jQDM('#dmcontentR').insertBefore(jQDM('#dmcontentL'));
	  } else {
		  jQDM('#dmmobiletopind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtotop'));
		  jQDM('#dmmobilebottomind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtobottom'));	  
		  jQDM('#df'+currDMDFID).html(''); 	
		  customTopDivPos();	  
	  }
    }
	
	if (ie == 8) {
            document.body.onresize = function() {
				if(jQDM(window).width() != startWidth){					
					if (jQDM(window).width() > 999) {
						if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
							jQDM('#dmcontentR').insertAfter(jQDM('#dmcontentL'));
						} else {
							if(jQDM('#df'+currDMDFID).is(':empty')){
								jQDM('#df'+currDMDFID).append(jQDM('#dmmobiletopind').html());
								jQDM('#df'+currDMDFID).append(jQDM('#dmmobilebottomind').html());
								jQDM('#dmmobiletopind').html('');
								jQDM('#dmmobilebottomind').html('');
							}
						}
						startWidth = jQDM(window).width();
					} else{	
						if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
							jQDM('#dmcontentR').insertBefore(jQDM('#dmcontentL'));
						} else {
							if(!jQDM('#df'+currDMDFID).is(':empty')){
								jQDM('#dmmobiletopind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtotop'));
								jQDM('#dmmobilebottomind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtobottom'));
								jQDM('#df'+currDMDFID).html('');								
							}
						}
						startWidth = jQDM(window).width();
					} 
					rightColReorder();
				}
			};
		} else {
            jQDM(window).resize(function() {				
				if(jQDM(window).width() != startWidth){					
					if (jQDM(window).width() > 999) {
						if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
							jQDM('#dmcontentR').insertAfter(jQDM('#dmcontentL'));
						} else {
							if(jQDM('#df'+currDMDFID).is(':empty')){
								jQDM('#df'+currDMDFID).append(jQDM('#dmmobiletopind').html());
								jQDM('#df'+currDMDFID).append(jQDM('#dmmobilebottomind').html());
								jQDM('#dmmobiletopind').html('');
								jQDM('#dmmobilebottomind').html('');
							}											
						}
						startWidth = jQDM(window).width();
					} else {
						if((jQDM('#df'+currDMDFID).hasClass('mobiletop')) && (jQDM('#df'+currDMDFID).is(':visible'))){
							jQDM('#dmcontentR').insertBefore(jQDM('#dmcontentL'));
						} else {
							if(!jQDM('#df'+currDMDFID).is(':empty')){
								jQDM('#dmmobiletopind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtotop'));
								jQDM('#dmmobilebottomind').append(jQDM('#df'+currDMDFID+' > .dmrightitemtobottom'));
								jQDM('#df'+currDMDFID).html('');								
							}
						}
						startWidth = jQDM(window).width();
					}
					rightColReorder();
				}				
            });
		}
		
		        

}
function rightColReorder(){
	if (jQDM(window).width() > 999) {
		var rcolamt = jQDM('#df'+currDMDFID+' > .dmrightcolitem').length;
		var prevRight;
		var nextRight;
		for (var a=1; a<=rcolamt; a++){
			whichRightNum = a;
			prevRight = a-1;
			nextRight = a+1;
			if(jQDM('#df'+currDMDFID+' > .right'+prevRight).length){
				jQDM('#df'+currDMDFID+' > .right'+a).insertAfter(jQDM('#df'+currDMDFID+' > .right'+prevRight));	
			} else {
				jQDM('#df'+currDMDFID+' > .right'+a).insertBefore(jQDM('#df'+currDMDFID+' > .right'+nextRight));
			}
		}
	} else {
		customTopDivPos();
	}
}

function customTopDivPos(){
	
	if(jQDM('#dfconfig'+currDMDFID).length){
			if(jQDM('#dfconfig'+currDMDFID+' .enforcemobilebottomtop').length){
				var enforceWhich = jQDM.trim(jQDM('#dfconfig'+currDMDFID+' .enforcemobilebottomtop').text());
				jQDM('#df'+currDMDFID+' > .right'+enforceWhich).insertBefore(jQDM('#dmmobilebottomind .dmrightcolitem:eq(0)'));
				
			} 
			if(jQDM('#dfconfig'+currDMDFID+' .enforcemobiletoptop').length){
				var enforceWhich = jQDM.trim(jQDM('#dfconfig'+currDMDFID+' .enforcemobiletoptop').text());
				jQDM('#df'+currDMDFID+' > .right'+enforceWhich).insertBefore(jQDM('#dmmobiletopind .dmrightcolitem:eq(0)')); 
				
			}
	} else {
		//set 3 always to top of bottom per request only when class is define
		if(jQDM('#df'+currDMDFID+' > .right3').hasClass('dmrightitemtobottom')){			
			jQDM('#df'+currDMDFID+' > .right3').insertBefore(jQDM('#dmmobilebottomind .dmrightcolitem:eq(0)')); 			 
		}
	}
}

function renderRightCol(whichDMDFID){
	jQDM('#df'+whichDMDFID).show();
	jQDM('#dfheader'+whichDMDFID).show();
	if(ie != 8){
		if(getURLParameter("showbgvid")==='y'){			
			if(jQDM('#dfvid'+whichDMDFID).length){
				var iOS = /iPad|iPhone|iPod/.test(navigator.platform);
				if( iOS ) {
					if(jQDM('#dfbg'+whichDMDFID).length){
						jQDM.backstretch(jQDM.trim(jQDM('#dfbg'+whichDMDFID).text()));
						jQDM('#df'+whichDMDFID).css({'background-color':'#fef8ef','padding':'10px'});
						jQDM('#dfheader'+whichDMDFID).css({'text-shadow':'2px 2px #000','color':'#fff'});
						jQDM('#dmfooter p').css('color','#fff');
						jQDM('#dmfooter a').css('color','#fff');
						jQDM('.dm-popout p').css('color','#000');
						jQDM('.dm-popout a').css('color','#007788');
					}
				} else{
					var vidPoster = jQDM.trim(jQDM('#dfvid'+whichDMDFID+' .dfvidposter').text());
					var vidOGV = jQDM.trim(jQDM('#dfvid'+whichDMDFID+' .dfvidogv').text());
					var vidMP4 = jQDM.trim(jQDM('#dfvid'+whichDMDFID+' .dfvidmp4').text());
					var vidWEBM = jQDM.trim(jQDM('#dfvid'+whichDMDFID+' .dfvidwebm').text());
					var builtVideo="<video id='bgvid' autoplay loop muted  preload='none' poster='"+vidPoster+"' style='background: url('"+vidPoster+"') no-repeat; background-size: cover;'><source src='"+vidMP4+"' type='video/mp4' /><source src='"+vidWEBM+"' type='video/webm' /><source src='"+vidOGV+"' type='video/ogg' /></video>";
					jQDM(builtVideo).insertBefore(jQDM('#dmheader'));
					jQDM('#df'+whichDMDFID).css({'background-color':'#fef8ef','padding':'10px'});
					jQDM('#dfheader'+whichDMDFID).css({'text-shadow':'2px 2px #000','color':'#fff'});
					jQDM('#dmfooter p').css('color','#fff');
					jQDM('#dmfooter a').css('color','#fff');
					jQDM('.dm-popout p').css('color','#000');
					jQDM('.dm-popout a').css('color','#007788');
				}					
			}						
		} else {
			if(jQDM('#dfbg'+whichDMDFID).length){
				jQDM.backstretch(jQDM.trim(jQDM('#dfbg'+whichDMDFID).text()));
				jQDM('#df'+whichDMDFID).css({'background-color':'#fef8ef','padding':'10px'});
				jQDM('#dfheader'+whichDMDFID).css({'text-shadow':'2px 2px #000','color':'#fff'});
				jQDM('#dmfooter p').css('color','#fff');
				jQDM('#dmfooter a').css('color','#fff');
				jQDM('.dm-popout p').css('color','#000');
				jQDM('.dm-popout a').css('color','#007788');
			}
		}	
	}
}

function magnificPopupsHandler(){
	 jQDM('.magpop').magnificPopup({
            type: 'inline',
            closeBtnInside: true
        });
}

function doPlaceHolder(){
	jQDM('#billing_first_namename').prop('placeholder',jQDM.trim(jQDM("label[for='billing_first_namename']").text()));
	jQDM('#billing_last_namename').prop('placeholder',jQDM.trim(jQDM("label[for='billing_last_namename']").text()));
	jQDM('#donor_email_addressname').prop('placeholder',jQDM.trim(jQDM("label[for='donor_email_addressname']").text()));
	jQDM('#billing_addr_street1name').prop('placeholder',jQDM.trim(jQDM("label[for='billing_addr_street1name']").text()));
	jQDM('#billing_addr_street2name').prop('placeholder',jQDM.trim(jQDM("label[for='billing_addr_street2name']").text()));
	jQDM('#billing_addr_cityname').prop('placeholder',jQDM.trim(jQDM("label[for='billing_addr_cityname']").text()));
	jQDM('#billing_addr_zipname').prop('placeholder',jQDM.trim(jQDM("label[for='billing_addr_zipname']").text()));
	jQDM('#billing_addr_state option:eq(0)').text(jQDM.trim(jQDM("label[for='billing_addr_state']").text()));
	jQDM("label[for='billing_first_namename']").hide();
	jQDM("label[for='billing_last_namename']").hide();
	jQDM("label[for='donor_email_addressname']").hide();
	jQDM("label[for='billing_addr_street1name']").hide();
	jQDM("label[for='billing_addr_street2name']").hide();
	jQDM("label[for='billing_addr_cityname']").hide();
	jQDM("label[for='billing_addr_zipname']").hide();
	jQDM("label[for='billing_addr_state']").hide();
	
	jQDM('#tribute_type option:eq(0)').text(jQDM.trim(jQDM("label[for='tribute_type']").text()));
	jQDM("label[for='tribute_type']").hide();
	jQDM('#tribute_honoree_first_namename').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_honoree_first_namename']").text()));
	jQDM("label[for='tribute_honoree_first_namename']").hide();
	jQDM('#tribute_honoree_last_namename').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_honoree_last_namename']").text()));
	jQDM("label[for='tribute_honoree_last_namename']").hide();
	jQDM('#tribute_ecard_subjectname').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_ecard_subjectname']").text()));
	jQDM("label[for='tribute_ecard_subjectname']").hide();
	jQDM('#tribute_ecard_messagename').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_ecard_messagename']").text()));
	jQDM("label[for='tribute_ecard_messagename']").hide();
	jQDM('#ecard_recpientsname').prop('placeholder',jQDM.trim(jQDM("label[for='ecard_recpientsname']").text()));
	jQDM("label[for='ecard_recpientsname']").hide();
	jQDM('<sup style="clear:both;">Separate email addresses by commas</sup>').insertAfter(jQDM('#ecard_recpientsname'));
	
	jQDM('#recipient_name_s__input').prop('placeholder',jQDM.trim(jQDM("label[for='recipient_name_s__input']").text()));
	jQDM("label[for='recipient_name_s__input']").hide();
	
	
	jQDM('#tribute_signaturename').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_signaturename']").text()));
	jQDM("label[for='tribute_signaturename']").hide();
	
	jQDM('#memorial-recipient_first_name_input').prop('placeholder',jQDM.trim(jQDM("label[for='memorial-recipient_first_name_input']").text()));
	jQDM("label[for='memorial-recipient_first_name_input']").hide();
	jQDM('#memorial-recipient_last_name_input').prop('placeholder',jQDM.trim(jQDM("label[for='memorial-recipient_last_name_input']").text()));
	jQDM("label[for='memorial-recipient_last_name_input']").hide();
	
	jQDM('#tribute_notify_recip_street1name').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_notify_recip_street1name']").text()));
	jQDM("label[for='tribute_notify_recip_street1name']").hide();		
	
	jQDM('#tribute_notify_recip_street2name').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_notify_recip_street2name']").text()));
	jQDM("label[for='tribute_notify_recip_street2name']").hide();
	
	jQDM('#tribute_notify_recip_cityname').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_notify_recip_cityname']").text()));
	jQDM("label[for='tribute_notify_recip_cityname']").hide();
	
	jQDM('#tribute_notify_recip_zipname').prop('placeholder',jQDM.trim(jQDM("label[for='tribute_notify_recip_zipname']").text()));
	jQDM("label[for='tribute_notify_recip_zipname']").hide();
	
	jQDM('#tribute_notify_recip_state option:eq(0)').text(jQDM.trim(jQDM("label[for='tribute_notify_recip_state']").text()));
	jQDM("label[for='tribute_notify_recip_state']").hide();
	jQDM("label[for='tribute_notify_recip_country']").hide();
	
	
	
	//jQDM('#responsive_payment_typecc_numbername').prop('placeholder',jQDM.trim(jQDM("label[for='responsive_payment_typecc_numbername']").text()));
	jQDM('#responsive_payment_typecc_numbername').prop('placeholder','Credit Card Number');
	//jQDM('#responsive_payment_typecc_cvvname').prop('placeholder',jQDM.trim(jQDM("label[for='responsive_payment_typecc_cvvname']").text()));
	jQDM('#responsive_payment_typecc_cvvname').prop('placeholder','CVV');
	jQDM("label[for='responsive_payment_typecc_numbername']").hide();
	jQDM("label[for='responsive_payment_typecc_cvvname']").hide();
	jQDM("label[for='billing_addr_country']").hide();
	jQDM('.field-required').hide();
	jQDM("label[for='responsive_payment_typecc_exp_date_MONTH']").hide();
}

function cstmFormValidation(){
	var askLvlLength = jQDM('.donation-level-label-container').length;	
	
	//check first what user selected ask level and put the correct active tab
	for(var w=0;w<askLvlLength;w++){		
			if(jQDM('.donation-level-label-container:eq('+w+')').hasClass('active')){
				if(jQDM('.donation-level-label-container:eq('+w+')').closest('.donation-level-container').hasClass('donOneTime')){
					jQDM('.askLvlTabs').removeClass('activeTab');
					jQDM('#tabOneTime').addClass('activeTab');
					jQDM('.donOneTime').show();
					jQDM('.donMonthly').hide();
					PaypalHandler(1);
					PremiumHandler();
				}else {
					jQDM('.askLvlTabs').removeClass('activeTab');
					jQDM('#tabRecurring').addClass('activeTab');
					jQDM('.donOneTime').hide();
					jQDM('.donMonthly').show();
					PaypalHandler(2);
					PremiumHandler();
				}
			}		
	}
	
	//if recurring and credit card info is empty	
	if(jQDM('#tabRecurring').hasClass('activeTab')){
		if((jQDM.trim(jQDM('#responsive_payment_typecc_numbername').val()) === '')||(jQDM.trim(jQDM('#responsive_payment_typecc_cvvname').val()) === '')){			
			//alert('Please provide credit card payment information');	
			jQDM.magnificPopup.open({
				  items: {
					  src: '#monthlycconly',
					  type: 'inline'
				  }      
  			});
			return false;
		}
	}
	
	//memorial and honor notification
	if(jQDM('#gift_information_input').length){
		if (jQDM.trim(jQDM('#gift_information_input').val()) === 'ecard'){
			
			if(jQDM.trim(jQDM('#recipient_name_s__input').val()) === ''){	
				jQDM('#recipient_name_s__input').val('N/A');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_first_name_input').val()) === ''){
				jQDM('#memorial-recipient_first_name_input').val('N/A');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_last_name_input').val()) === ''){
				jQDM('#memorial-recipient_last_name_input').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_street1name').val()) === ''){
				jQDM('#tribute_notify_recip_street1name').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_cityname').val()) === ''){
				jQDM('#tribute_notify_recip_cityname').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_zipname').val()) === ''){
				jQDM('#tribute_notify_recip_zipname').val('N/A');
			}			
			
		} else if (jQDM.trim(jQDM('#gift_information_input').val()) === 'printcard'){		
			
		} else {
			if(jQDM.trim(jQDM('#recipient_name_s__input').val()) === ''){
				jQDM('#recipient_name_s__input').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_ecard_messagename').val()) === ''){
				jQDM('#tribute_ecard_messagename').val('N/A');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_first_name_input').val()) === ''){
				jQDM('#memorial-recipient_first_name_input').val('N/A');
			}
			if(jQDM.trim(jQDM('#memorial-recipient_last_name_input').val()) === ''){
				jQDM('#memorial-recipient_last_name_input').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_street1name').val()) === ''){
				jQDM('#tribute_notify_recip_street1name').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_cityname').val()) === ''){
				jQDM('#tribute_notify_recip_cityname').val('N/A');
			}
			if(jQDM.trim(jQDM('#tribute_notify_recip_zipname').val()) === ''){
				jQDM('#tribute_notify_recip_zipname').val('N/A');
			}			
		}
	}
	
	
}
function regroupAskLvl(){
	if (window.console) {		
		console.log("Ask Level Length: "+jQDM('.donation-level-label-container').length);
	}	
	var askLvlLength = jQDM('.donation-level-label-container').length;
	var askLvlType = 2; //2 is one time and monthly (default), 0 is one time only, 1 is monthly only
	var firstOther = 0;  
	var currLblTxt;
	var askLvlLastIndex = askLvlLength - 1;
	
	for(var w=0;w<askLvlLength;w++){			
		currLblTxt = jQDM.trim(jQDM('.donation-level-label-container:eq('+w+')').text());
		
		//determine when there is only monthly ask level
		if((w==0)&&(currLblTxt.indexOf("-mth")!= -1)){			
			jQDM('.askLvlTabs').removeClass('activeTab');
			jQDM('#tabRecurring').addClass('activeTab');
			jQDM('#tabHeader').hide();
			askLvlType = 1;
		} else {		
			if((currLblTxt.indexOf("Other")== -1)&&(firstOther != 1)&&(askLvlType != 1)){
				jQDM('.donation-level-label-container:eq('+w+')').closest('.donation-level-container').addClass('donOneTime');
				if(jQDM('.donation-level-label-container:eq('+w+')').hasClass('active')){
					jQDM('.askLvlTabs').removeClass('activeTab');
					jQDM('#tabOneTime').addClass('activeTab');
				}
			} else if((currLblTxt.indexOf("Other")!= -1)&&(firstOther != 1)&&(askLvlType != 1)){
				jQDM('.donation-level-label-container:eq('+w+')').closest('.donation-level-container').addClass('donOneTime');
				firstOther = 1;	
				if(jQDM('.donation-level-label-container:eq('+w+')').hasClass('active')){
					jQDM('.askLvlTabs').removeClass('activeTab');
					jQDM('#tabOneTime').addClass('activeTab');
				}
				//check if there is only one time no monthly
				if(w==askLvlLastIndex){
					jQDM('#tabHeader').hide();
					askLvlType = 0;
					if (ie == 8){
						jQDM('.donation-level-label-container:eq('+w+')').closest('.form-content').css('width','250px');
					}
				}
				
			} else { 
				if (askLvlType == 2) {
					jQDM('.donation-level-label-container:eq('+w+')').closest('.donation-level-container').addClass('donMonthly');
					jQDM('.donation-level-label-container:eq('+w+')').text(currLblTxt.replace('-mth',''));
					if(jQDM('.donation-level-label-container:eq('+w+')').hasClass('active')){
						jQDM('.askLvlTabs').removeClass('activeTab');
						jQDM('#tabRecurring').addClass('activeTab');
					}
					if(w==askLvlLastIndex){
						if (ie == 8){
							jQDM('.donation-level-label-container:eq('+w+')').closest('.form-content').css('width','250px');
						}
					}										
				}
			}
		}
		
		if(askLvlType == 1){
			jQDM('.donation-level-label-container:eq('+w+')').closest('.donation-level-container').addClass('donMonthly');
			jQDM('.donation-level-label-container:eq('+w+')').text(currLblTxt.replace('-mth',''));
			if(w==askLvlLastIndex){
				if (ie == 8){
					jQDM('.donation-level-label-container:eq('+w+')').closest('.form-content').css('width','250px');
				}
			}
		} 
		
		
	}

	if(jQDM('#tabRecurring').hasClass('activeTab')){
		jQDM('.donOneTime').hide();
		jQDM('.donMonthly').show();
		PaypalHandler(2);
	} else {	
	    jQDM('#tabOneTime').addClass('activeTab');		
		jQDM('.donOneTime').show();
		jQDM('.donMonthly').hide();
		PaypalHandler(1);
	}
	
	if(askLvlType == 2){
		PremiumHandler();
	}
	
	//click handler
	jQDM('#tabOneTime').click(function(){
		jQDM('.askLvlTabs').removeClass('activeTab');
		jQDM(this).addClass('activeTab');
		jQDM('.donOneTime').show();
		jQDM('.donMonthly').hide();
		PaypalHandler(1);
		PremiumHandler();
	});
	jQDM('#tabRecurring').click(function(){
		jQDM('.askLvlTabs').removeClass('activeTab');
		jQDM(this).addClass('activeTab');
		jQDM('.donOneTime').hide();
		jQDM('.donMonthly').show();
		PaypalHandler(2);
		PremiumHandler();
	});
}

function PremiumHandler(){	
		//hide premium availability addresing OTHER custom - setup
		if(jQDM('#dfconfig'+currDMDFID).length){
				if(jQDM('#dfconfig'+currDMDFID+' .premiummonthly').length){
					if(jQDM.trim(jQDM('#dfconfig'+currDMDFID+' .premiummonthly').text()) == 0){
						if((jQDM('#tabRecurring').hasClass('activeTab')) && (jQDM('#tabRecurring').is(':visible'))){
							jQDM('#premium_selector_radio_row_no_premium_available').hide();
							jQDM('#premium_selector_row').hide();
						} else {
							jQDM('#premium_selector_radio_row_no_premium_available').show();
							jQDM('#premium_selector_row').show();
						}
					} 
				} 
				if(jQDM('#dfconfig'+currDMDFID+' .premiumonetime').length){								
					if(jQDM.trim(jQDM('#dfconfig'+currDMDFID+' .premiumonetime').text()) == 0){
						if((jQDM('#tabOneTime').hasClass('activeTab')) && (jQDM('#tabOneTime').is(':visible'))){
							jQDM('#premium_selector_radio_row_no_premium_available').hide();
							jQDM('#premium_selector_row').hide();
						} else {
							jQDM('#premium_selector_radio_row_no_premium_available').show();
							jQDM('#premium_selector_row').show();
						}
					}
				}
		}
	
}

function PaypalHandler(whichMode){	
	switch(whichMode){
		case 1:
			jQDM('span.external-payment').css({'position':'relative','margin-top':'auto'});			
		break;
		case 2:			
			jQDM('span.external-payment').css({'position':'absolute','margin-top':'-9999px'});
			jQDM('span.internal-payment span.payment-type-option').trigger('click');
			jQDM('span.internal-payment span.payment-type-option').addClass('selected');
			jQDM('span.external-payment span.payment-type-option').removeClass('selected');	
			jQDM('#payment_cc_container').show();
			jQDM('input[name="responsive_payment_typepay_typeradio"]').val(['credit']);
		break;
	}
}

//Get Internet Explorer Version 7 - 11
function getInternetExplorerVersion() {
        var rv = -1; // Return value assumes failure.
        var isIE11 = !!navigator.userAgent.match(/Trident.*rv[ :]*11\./);
        if (navigator.appName == 'Microsoft Internet Explorer') {
            var ua = navigator.userAgent;
            var re = new RegExp("MSIE ([0-9]{1,}[\.0-9]{0,})");
            var re2 = new RegExp("MSIE ([10]{1,}[\.10]{0,})");
            if (re.exec(ua) != null) {
                rv = parseFloat(RegExp.$1);
            } else if (re2.exec(ua) != null) {
                rv = parseFloat(RegExp.$1);
            }
        }
        if (isIE11) {
            rv = 11;
        }
        return rv;
}

//Get URL Parameter
function getURLParameter(name) {
        return decodeURI(
            (RegExp(name + '=' + '(.+?)(&|$)').exec(location.search) || [, null])[1]
        );
}
