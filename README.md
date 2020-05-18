# utl-python-AI-color-frequencies-in-an-image
Python AI color frequencies in an image 
    Python AI color frequencies in an image                                                                              
                                                                                                                         
    github                                                                                                               
    https://tinyurl.com/yaz3ua2n                                                                                         
    https://github.com/rogerjdeangelis/utl-python-AI-color-frequencies-in-an-image                                       
                                                                                                                         
    related repo                                                                                                         
    https://github.com/rogerjdeangelis?tab=repositories&q=image&type=&language=                                          
                                                                                                                         
    SOAPBOX ON                                                                                                           
                                                                                                                         
     Python is a legend unto itself.                                                                                     
     Python does not interface easily with other languages.                                                              
                                                                                                                         
     I spent a lot of time trying to output                                                                              
     a panda dataframe to a SAS V5 export file.                                                                          
     I finally gave up.                                                                                                  
                                                                                                                         
     Pyton has too many datastructures and data types, worse than R.                                                     
                                                                                                                         
     You really only need two datatypes                                                                                  
                                                                                                                         
        128 bit floats (with SAS length options 3, 4 ,5 ,6 7 8, 9, 10 ,11, 12, 13, 14. 15. 16)                           
        long character.                                                                                                  
                                                                                                                         
        Python also needs peek and poke like SAS so you can poke these crazy datatypes into a string                     
        and contert the binary info in SAS.                                                                              
                                                                                                                         
        Perhaps two data structures                                                                                      
           Retangle Table (SAS dataset)                                                                                  
           List but only a list of retangular tables (SAS datasets)                                                      
                                                                                                                         
     Itel could simplify, speed up and reduce silicon chip real-estate by eliminating                                    
     integer aritmetic and concentrated on floating point arithmetic. Less real-estate                                   
     means easier cooling.                                                                                               
                                                                                                                         
    SOAPBOX OFF                                                                                                          
                                                                                                                         
    Stackoverflow                                                                                                        
    https://tinyurl.com/y97emt5a                                                                                         
    https://stackoverflow.com/questions/61833435/is-there-an-efficient-way-to-bin-the-main-colors-from-an-rgb-image      
                                                                                                                         
    *_                   _                                                                                               
    (_)_ __  _ __  _   _| |_                                                                                             
    | | '_ \| '_ \| | | | __|                                                                                            
    | | | | | |_) | |_| | |_                                                                                             
    |_|_| |_| .__/ \__,_|\__|                                                                                            
            |_|                                                                                                          
    ;                                                                                                                    
                                                                                                                         
    Pie chart with three slices and RGB colors Red, Green and Blue                                                       
                                                                                                                         
                                                                                                                         
    filename grafout 'd:png\pie3.png';                                                                                   
    goptions reset=all gsfname=grafout gsfmode=replace device=png hsize=1in vsize=1in;                                   
                                                                                                                         
    pattern1  color=CXFF0000;  * red;                                                                                    
    pattern2  color=CX00FF00;  * green;                                                                                  
    pattern3  color=CX0000FF;  * blue;                                                                                   
                                                                                                                         
    proc gchart data=sashelp.cars;                                                                                       
    PIE origin/ value=none                                                                                               
                  noheading;                                                                                             
    run;quit;                                                                                                            
    goptions reset=all;                                                                                                  
                                                                                                                         
    options ls=72 ps=44;                                                                                                 
    proc chart data=sashelp.cars;                                                                                        
    pie origin;                                                                                                          
    run;quit;                                                                                                            
                                                                                                                         
                         *************                                                                                   
                  *******             ****                                                                               
                **                        ***                                                                            
              **                             **                                                                          
            ** ..                              **                                                                        
           *     .       __ _ _ __ ___  ___ _ __**                                                                       
         **        .    / _` | '__/ _ \/ _ \ '_ \ *                                                                      
         *          .  | (_| | | |  __/  __/ | | | **                                                                    
        *            .  \__, |_|  \___|\___|_| |_|  *                                                                    
       **             . |___/                        *                                                                   
       *                .                            **                                                                  
      **                 ..                           *                                                                  
      *               _    .                          **                                                                 
      *  _ __ ___  __| |     .                         *                                                                 
      * | '__/ _ \/ _` |      .                        *                                                                 
      * | | |  __/ (_| |       + . . .. . .. . .. . .. *                                                                 
      * |_|  \___|\__,_|      .                        *                                                                 
      **                    ..                         *                                                                 
       *                    .    _     _              **                                                                 
       **                  .    | |__ | |_   _  ___    *                                                                 
        *                 .     | '_ \| | | | |/ _ \  **                                                                 
         *                .     | |_) | | |_| |  __/  *                                                                  
          *            ..       |_.__/|_|\__,_|\___|  *                                                                  
           *          .                              *                                                                   
            **      .                              **                                                                    
              **   .                             **                                                                      
                **.                            **                                                                        
                  ***                      ***                                                                           
                      ****             ****                                                                              
                          *************                                                                                  
    *            _               _                                                                                       
      ___  _   _| |_ _ __  _   _| |_                                                                                     
     / _ \| | | | __| '_ \| | | | __|                                                                                    
    | (_) | |_| | |_| |_) | |_| | |_                                                                                     
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                    
                    |_|                                                                                                  
    ;                                                                                                                    
                                                                                                                         
                                                                                                                         
    PYTHON OUTPUT                                                                                                        
    =============                                                                                                        
                                                                                                                         
    Number of colors = 130                                                                                               
                                                                                                                         
    Number of cells  = 96*96 = 9216                                                                                      
    <PIL.Image.Image image mode=RGB size=96x96 at 0x135CDF7D2E0>                                                         
                                                                                                                         
    TOP 30 Frequencies                                                                                                   
                                                                                                                         
    0     (3210, (255, 255, 255))                                                                                        
    1         (1996, (255, 0, 0))                                                                                        
    2         (1886, (0, 0, 255))                                                                                        
    3         (1565, (0, 255, 0))                                                                                        
    4            (147, (0, 0, 0))                                                                                        
    5            (41, (0, 0, 85))                                                                                        
    6           (23, (0, 0, 170))                                                                                        
    7           (12, (0, 75, 56))                                                                                        
    8            (12, (0, 51, 0))                                                                                        
    9            (12, (51, 0, 0))                                                                                        
    10      (11, (113, 113, 170))                                                                                        
    11          (11, (0, 102, 0))                                                                                        
    12           (10, (0, 85, 0))                                                                                        
    13           (10, (85, 0, 0))                                                                                        
    14           (9, (0, 0, 127))                                                                                        
    15       (8, (170, 113, 113))                                                                                        
    16           (8, (170, 0, 0))                                                                                        
    17           (8, (102, 0, 0))                                                                                        
    18       (6, (163, 204, 163))                                                                                        
    19       (6, (204, 163, 163))                                                                                        
    20         (6, (91, 153, 91))                                                                                        
    21         (6, (153, 91, 91))                                                                                        
    22           (6, (0, 204, 0))                                                                                        
    23           (6, (0, 153, 0))                                                                                        
    24         (6, (64, 64, 128))                                                                                        
    25            (6, (0, 42, 0))                                                                                        
    26          (6, (85, 28, 28))                                                                                        
    27           (6, (204, 0, 0))                                                                                        
    28           (6, (153, 0, 0))                                                                                        
    29       (5, (113, 170, 113))                                                                                        
    dtype: object                                                                                                        
                                                                                                                         
    SAS OUTPUT                                                                                                           
    ==========                                                                                                           
                                                                                                                         
    Up to 40 obs WORK.WANT total obs=30                                                                                  
                                                                                                                         
          COUNT   COLOR                                                                                                  
          TOTAL   COUNT_  COLOR                                                                                          
    Obs   CELLS     CUM   COUNT     COLOR    (agrees with SAS pattern statement)                                         
                                                                                                                         
      1    9216    3210    3210    CXFFFFFF  White                                                                       
                                                                                                                         
      2    9216    5206    1996    CXFF0000  pattern1  color=CXFF0000;  * red;                                           
      3    9216    7092    1886    CX0000FF  pattern2  color=CX0000FF;  * green;                                         
      4    9216    8657    1565    CX00FF00  pattern3  color=CX00FF00;  * blue;                                          
                                                                                                                         
      5    9216    8804     147    CX000000                                                                              
      6    9216    8845      41    CX000055                                                                              
      7    9216    8868      23    CX0000AA                                                                              
      8    9216    8880      12    CX004B38                                                                              
      9    9216    8892      12    CX003300                                                                              
     10    9216    8904      12    CX330000                                                                              
     11    9216    8915      11    CX7171AA                                                                              
     12    9216    8926      11    CX006600                                                                              
     13    9216    8936      10    CX005500                                                                              
     14    9216    8946      10    CX550000                                                                              
     15    9216    8955       9    CX00007F                                                                              
     16    9216    8963       8    CXAA7171                                                                              
     17    9216    8971       8    CXAA0000                                                                              
     18    9216    8979       8    CX660000                                                                              
     19    9216    8985       6    CXA3CCA3                                                                              
     20    9216    8991       6    CXCCA3A3                                                                              
     21    9216    8997       6    CX5B995B                                                                              
     22    9216    9003       6    CX995B5B                                                                              
     23    9216    9009       6    CX00CC00                                                                              
     24    9216    9015       6    CX009900                                                                              
     25    9216    9021       6    CX404080                                                                              
     26    9216    9027       6    CX002A00                                                                              
     27    9216    9033       6    CX551C1C                                                                              
     28    9216    9039       6    CXCC0000                                                                              
     29    9216    9045       6    CX990000                                                                              
     30    9216    9050       5    CX71AA71                                                                              
                                                                                                                         
    *                                                                                                                    
     _ __  _ __ ___   ___ ___  ___ ___                                                                                   
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                                  
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                  
    | .__/|_|  \___/ \___\___||___/___/                                                                                  
    |_|                                                                                                                  
    ;                                                                                                                    
                                                                                                                         
    %utlfkil(d:/txt/file.txt);                                                                                           
                                                                                                                         
    %utl_submit_py64_38('                                                                                                
    import pyreadstat;                                                                                                   
    from PIL import Image;                                                                                               
    import pandas as pd;                                                                                                 
    import numpy;                                                                                                        
    img = Image.open("d:png\pie3.png");                                                                                  
    im_rgb = img.convert("RGB");                                                                                         
    colors = im_rgb.getcolors(maxcolors=200000);                                                                         
    print(len(colors));                                                                                                  
    colors = sorted(colors, key = lambda x:-x[0]);                                                                       
    print(im_rgb);                                                                                                       
    s = pd.Series(data=colors[0:30]);                                                                                    
    print(s);                                                                                                            
    with open("d:/txt/file.txt", "a") as f:;                                                                             
    .   print(s, file=f);                                                                                                
    ');                                                                                                                  
                                                                                                                         
    data want;                                                                                                           
     retain count_cum 0;                                                                                                 
     infile "d:/txt/file.txt";                                                                                           
     input @4;                                                                                                           
     count_total=96*96;                                                                                                  
     count=input(scan(_infile_,2,'(,'),8.);;                                                                             
     count_cum=count_cum+count;                                                                                          
     Rc=compress(scan(_infile_,2,','),'()');                                                                             
     Gc=compress(scan(_infile_,3,','),'()');                                                                             
     Bc=compress(scan(_infile_,4,','),'()');                                                                             
     R=put(inputn(rc,4.),hex2.);                                                                                         
     g=put(inputn(gc,4.),hex2.);                                                                                         
     b=put(inputn(bc,4.),hex2.);                                                                                         
     color=cats('CX',r,g,b);                                                                                             
     keep count: color;                                                                                                  
     output;                                                                                                             
     if _n_=30 then stop;                                                                                                
    run;quit;                                                                                                            
                                                                                                                         
