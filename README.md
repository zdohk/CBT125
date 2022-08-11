~~~~~~~~~~~~~~~~

//***FILE 125 IS FROM THE STATE OF CONNECTICUT AND CONTAINS SEVERAL *   FILE 125
//*           SAS PROGRAMS.  THE FOLLOWING IS A LIST OF MEMBERS IN  *   FILE 125
//*           THIS FILE.                                            *   FILE 125
//*                                                                 *   FILE 125
//*           $$README  IMPORTANT INFORMATION. READ THIS BEFORE     *   FILE 125
//*                     USING.                                      *   FILE 125
//*           $FILE1    INSTRUCTIONS AND JCL TO UNLOAD TAPE         *   FILE 125
//*           $MEMINFO  DOCUMENTATION MEMBER                        *   FILE 125
//*           $SASDOC   SHORT DECRIPTION OF SYSTEM                  *   FILE 125
//*           ALLOCPDS  JCL TO ALLOCATE SOURCE PDS                  *   FILE 125
//*           ALLOCSAS  JCL TO ALLOCATE SAS DATASET                 *   FILE 125
//*           COPYDT    IEBGENER TO COPY SMF/RMF DATA FROM DISK TO  *   FILE 125
//*                     TAPE                                        *   FILE 125
//*           CPTOT     SAS PROGRAM TO READ SUMMARIZED RMF RECORDS  *   FILE 125
//*                     PRODUCED BY CPUT.                           *   FILE 125
//*           CPTOTJ    JCL TO RUN CPTOT IN BATCH.                  *   FILE 125
//*           CPUT      SAS PROGRAM TO READ RMF RECORDS. USED TO    *   FILE 125
//*                     FIND TOTAL UTIL.  OF A PHYSICAL PROCESSOR   *   FILE 125
//*                     COMPLEX.                                    *   FILE 125
//*           CPUTJ     JCL TO RUN CPUT IN BATCH                    *   FILE 125
//*           DOC1      LONG DESRIPTION OF SYSTEM                   *   FILE 125
//*           LOADTP    JCL TO LOAD TAPE WITH INSTRUCTIONS AND PDS  *   FILE 125
//*           RMF70     SAS PROGRAM TO READ RMF TYPE 70 RECS        *   FILE 125
//*           RMF70J    JCL TO RUN RMF70 IN BATCH                   *   FILE 125
//*           RMF70W    SAME AS RMF70 EXCEPT OUTPUT STATEMENTS ARE  *   FILE 125
//*                     DIFFERENT                                   *   FILE 125
//*           RMF70WJ   JCL TO RUN RMF70W IN BATCH                  *   FILE 125
//*           RMF71     SAS PROGRAM TO READ RMF TYPE 71 RECS        *   FILE 125
//*           RMF71J    JCL TO RUN RMF71 IN BATCH                   *   FILE 125
//*           RMF71W    SAME AS RMF71 EXCEPT OUTPUT STATEMENTS ARE  *   FILE 125
//*                     DIFFERENT                                   *   FILE 125
//*           RMF71WJ   JCL TO RUN RMF71W IN BATCH                  *   FILE 125
//*           RMF72     SAS PROGRAM TO READ RMF TYPE 72 RECS        *   FILE 125
//*           RMF72J    JCL TO RUN RMF72 IN BATCH                   *   FILE 125
//*           RMF72W    SAME AS RMF72 EXCEPT OUTPUT STATEMENTS ARE  *   FILE 125
//*                     DIFFERENT                                   *   FILE 125
//*           RMF72WJ   JCL TO RUN RMF72W IN BATCH                  *   FILE 125
//*           SORTWEEK  JCL TO SORT RMF RECORDS                     *   FILE 125
//*           UNLOAD    JCL TO UNLOAD INSTRUCTIONS AND SOURCE PDS   *   FILE 125
//*                     FROM TAPE                                   *   FILE 125
//*           XY9910    ASM PROGRAM TO PULL OFF RMF 70-79 RECORDS   *   FILE 125
//*                     FROM TAPE                                   *   FILE 125
//*           XY9910AS  JCL TO ASSEMBLE/LINK XY9910                 *   FILE 125
//*           XY9910J   JCL TO RUN PROGRAM XY9910                   *   FILE 125
//*                                                                 *   FILE 125
//*           THE MEMBERS BELOW ARE SAS PROGRAMS THAT GRAPH SOME OF *   FILE 125
//*           THE DATA SAVED IN THE SAS DATASET BY RMF70, RMF71,    *   FILE 125
//*           RMF72 AND OTHER DATA REDUCTION PROGRAMS.              *   FILE 125
//*                                                                 *   FILE 125
//*           MEMBER   DESCRIPTION                                  *   FILE 125
//*                                                                 *   FILE 125
//*           BATCH    JCL TO PRINT GRAPHS TO A LOCAL PRINTER(S)    *   FILE 125
//*                    WITHOUT HAVING TO USE TSO.                   *   FILE 125
//*           CPUCPW   2-DIM GRAPH OF AVERAGE CPU UTILIZATION BY    *   FILE 125
//*                    MACHINE. PLOTTED BY DAY, FOR ONE WEEK.       *   FILE 125
//*           CPUNDL   3-DIM GRAPH OF AVERAGE CPU UTILIZATION BY    *   FILE 125
//*                    MACHINE (SCATTER DIAGRAM). EACH RMF INTERVAL *   FILE 125
//*                    IS SHOWN AND GROUPED BY LOW, MED., OR HIGH   *   FILE 125
//*                    CPU UTILIZATION. BEST WHEN PRINTED IN COLOR. *   FILE 125
//*           CPUUT    2-DIM GRAPH OF AVERAGE CPU UTILIZATION BY    *   FILE 125
//*                    MACHINE. PLOTTED BY DAY.                     *   FILE 125
//*           D2BAV    2-DIM GRAPH OF AVERAGE BATCH USERS AND ASIDS *   FILE 125
//*                    OUT/READY. PLOTTED BY DAY.                   *   FILE 125
//*           D2BMM    2-DIM GRAPH OF AVERAGE MAX BATCH USERS.      *   FILE 125
//*           D2CPU    2-DIM GRAPH OF AVERAGE CPU UTILIZATION.      *   FILE 125
//*                    PLOTTED BY DAY.                              *   FILE 125
//*           D2PPS    2-DIM GRAPH OF PAGES PER SECOND.             *   FILE 125
//*                    PLOTTED BY DAY.                              *   FILE 125
//*           D2PPS2   2-DIM GRAPH OF PAGES PER SECOND FOR SYSTEM   *   FILE 125
//*                    2.  PLOTTED BY DAY.                          *   FILE 125
//*           D2PPS3   2-DIM GRAPH OF PAGES PER SECOND FOR SYSTEM   *   FILE 125
//*                    3.  PLOTTED BY DAY.                          *   FILE 125
//*           D2RT2    2-DIM GRAPH OF AVERAGE TSO RESPONSE TIME FOR *   FILE 125
//*                    ALL PERIODS AND ALSO THE AVERAGE. PLOTTED BY *   FILE 125
//*                    DAY.                                         *   FILE 125
//*           D2RT2P1  2-DIM GRAPH OF AVERAGE TSO RESPONSE FOR      *   FILE 125
//*                    PERFORMANCE GROUP 2, PERIOD 1 (TRIVIAL).     *   FILE 125
//*                    CAN BE USED FOR ANY PERFORMANCE GROUP BY     *   FILE 125
//*                    CHANGING THE INPUT. PLOTTED BY DAY.          *   FILE 125
//*           D2RT2H   2-DIM GRAPH OF AVERAGE TSO RESPONSE TIME FOR *   FILE 125
//*                    FIRST PERIOD.  X-AXIS IS 1/2 HOUR INTERVALS  *   FILE 125
//*                    STRUNG OUT BY DAY.  (I.E 9-4 DAY 1, 9-4 DAY  *   FILE 125
//*                    2, ETC.)                                     *   FILE 125
//*           D2TMM    2-DIM GRAPH OF AVERAGE OF MAX TSO USERS      *   FILE 125
//*                    LOGGED ON. PLOTTED BY DAY.                   *   FILE 125
//*           M1HH     SHOWS CPU UTILIZATION (BY MACHINE)           *   FILE 125
//*                    SUMMARIZED BY HOURS. GIVES MAX UTIL FOR 1    *   FILE 125
//*                    HOUR, HIGHEST HOURLY AVERAGE, AND MONTHLY    *   FILE 125
//*                    AVERAGE OF ALL THE HOURS.                    *   FILE 125
//*           PGSECC   3-DIM CONTOUR GRAPH OF PAGES/SEC BY HOUR BY  *   FILE 125
//*                    DAY.  NOT THE GREATEST.                      *   FILE 125
//*           PPS3D    3-DIM GRAPH OF PAGES/SEC BY HOUR BY DAY.     *   FILE 125
//*           PPS3DS   3-DIM SCATTER DIAGRAM OF PAGES/SEC BY HOUR   *   FILE 125
//*                    BY DAY.                                      *   FILE 125
//*           REGCPU   REGRESSION ANALYSIS OF CPU UTILIZATION.      *   FILE 125
//*                    BY DAY.                                      *   FILE 125
//*           RM1CPMAX REGRESSION ANALYSIS OF MAXIMUM CPU           *   FILE 125
//*                    UTILIZATION FOR ONE MACHINE.  BY DAY.        *   FILE 125
//*           RM1CPU   REGRESSION ANALYSIS OF TOTAL CPU UTILIZATION *   FILE 125
//*                    FOR ONE MACHINE.  BY DAY.                    *   FILE 125
//*           REGPPS1  REGRESSION ANALYSIS OF PAGES PER SECOND.     *   FILE 125
//*                    BY DAY.                                      *   FILE 125
//*           RT213D   3-DIM GRAPH OF AVERAGE TSO FIRST PERIOD      *   FILE 125
//*                    RESPONSE TIME.  BY 1/2 HOUR BY DAY.          *   FILE 125
//*                                                                 *   FILE 125
~~~~~~~~~~~~~~~~

