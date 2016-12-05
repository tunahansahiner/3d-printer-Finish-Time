# 3d-printer-Finish-Time


 // SD Card Progress bar and clock
 u8g.setFont(FONT_STATUSMENU);
 
 if (IS_SD_PRINTING)
   {
	// Progress bar
	u8g.drawBox(55,50, (unsigned int)( (71 * card.percentDone())/100) ,2);
  /*change this area */
	// Percent complete  added by tuna
	u8g.setPrintPos(55,47);
	u8g.print(itostr3(card.percentDone()));
	u8g.print("%"); // add finished by tuna
   }
    else {
			// do nothing
		 }
