________________________________________________________________________________
     
    ABOUT
________________________________________________________________________________

  HotLog.pas is the source file of a freeware LogFile manager. It works under D6
  & D7, and should work under D5 (which I can't test). It's latest version can be
  downloaded from :
         http://mapage.noos.fr/qnno/pages/delphi_en.htm  -  qnno@noos.fr)


  Enhancements, feedback and comments allways welcome,
  (c)Olivier Touzot ( QnnO@noos.fr )


________________________________________________________________________________

 Install and use 
________________________________________________________________________________

 Delphi 6 & 7 :
 --------------
  Simply unzip HotLog.pas in the directory of your project, and add it to the
  "uses" clauses of the units you want to use THotLog.
  For more detailed explanations, please see the .chm help file provided.

 Delphi 5 :
 ----------
  You will need the StrUtils.pas (& dcu) files from the provided
                "arstrutils - D5 users only.zip"

  This unit implements two functions : "LeftStr()" and "RightStr".
  It has been written by Alexis Rios and can be found at Torry's place
  (Alexis' web pages seem to no longer exists.)

  You should copy both files (StrUtils.pas & StrUtils.dcu in a directory
  which path is known by your compiler (".\lib" is a good candidate).
  
  Femi Fadayomi, who did the port to D5 adds : "Users of JVCL can alo
  replace StrUtils with jvStrUtils to compile for D5."



________________________________________________________________________________
 
 Acknowledgment 
________________________________________________________________________________

  Special thanks go to:
    * Luis Gonzalo Constantini Von Rickel, who did a great fix in the
      FileCreate() function, and worked a lot on the visual feedback part.
      (see code)
    * Femi Fadayomi, who did add Delphi 5 support.
    * Robert Becker (rbecker@compuserve.com), who brought to us, hLog users,
      what was certainely the "most wanted" feature : HotLog can now be limited
      in size, and automatically opens a new file when a certain size limit is
      reached.
    * Guillaume Cornu, for fixing the GetRegValue() function ;
    * Oleg Danilov, who added the SetMemoLimit() procedure ;
    * Vittorio Loschi, who corrected the buggy SetFileName() procedure ;
    * "Sergueï" who fixed a sometimes incorrect initialization ;
    * Jean-Philippe R. who tracked and fixed a bug occuring in "append" mode ;
    
    ... And to all those of you who sent suggestions or encouragements.
    

________________________________________________________________________________

    History
________________________________________________________________________________


v 2.2 (2005-07-24 : Luis Gonzallo Constantini Von Rickel new enhancements,
                    and bug correction :
                    Faster Memo Cleanning, Stop Repainting During Process,
                    and do the Scroll to the Last Line of the Memo.
                    Luis Gonzalo Constantini Von Rickel TFileStream Object
                    Creating is placed outside try...finally block to avoid
                    Access Violation Exception if the object can not be created.                                        

v 2.1 (2005-07-17 : Delphi 5 support added by Femi Fadayomi.)

v 2.0 (2005-07-10 : It eventually happened ! Thanks to Robert Becker, HotLog is
                    now able to close the log file, and open a new one once a
                    given limit is reached. Many thanks to him to have worked
                    on that.)
                    
v 1.6 (2005-03-31 : Correction of the GetRegValue() function by Guillaume Cornu,
                    preventing attemps to read the byte [0] of a string.
                    (Looking for it on the web, I can see that I never pushed it
                    here, sorry about that.)

v 1.5 (2005-01-17 : One more enhancement by Oleg Danilov which allows  to limit
                    size of the memo (SetMemoLimit procedure)(Usefull if a 
                    program generates a HUGE output for a long time, or to avoid
                    problems with the old versions of the TMemo component
                    (32k limit)).      

v 1.4 (2004-11-17 : Usefull workaround brought by Luis Gonzalo Constantini Von
                    Rickel to override the limits of the FileCreate() function,
                    in order to emulate the use of a flag other than 
                    "fmShareExclusive".) (See his explanations at the beginning
                    of the writer thread.)                                    

v 1.3 (2004-10-02 : THLFileDef.SetFileName() procedure corrected by Vittorio
                    Loschi.)                                  

v 1.2 (2004-07-05 : Correction of the "fast start" problem by "Sergueï" :
                    When using hLog just after the call to StartLogging the
                    writer thread's queue could sometimes not yet exist, and the
                    very first lines were lost.)

v 1.1 (2004-06-28 : Correction of a bug signaled by Jean-Philippe R. which
                    occured in "append" mode, when the log file does not yet
                    exist)                                

v 1.0 (2004-03-22 : Online.)


