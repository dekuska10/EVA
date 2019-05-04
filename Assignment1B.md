Channels :
   Channels can be considered as container which  consists of information of the objects , for an image channels consists of edge , textures and other attritbutes of an object.A channel of an image can be divide into numbers channels which consists of all the attributes of an object in an image.

Kernel :
   They are called as filters , feature extractors where we extract the prominent features from an image . The kernel consists of values which can we used to extract the information by performing  matrix multiplication with the orginal image  

Why should we only (well mostly) use 3x3 Kernels?

     Using 3x3 kernels or an odd shaped kernels is because of the symmetry , since odd dimensioned kernels have a anchor      points it has 
     pixels surroudning it along with the center pixel point due to which matrix multiplicaiton is feasible . In odd dimesioned 
     kernel 3x3 is perffered to other dimensions like 5x5,7x7 is because of the computation time taken. 

     Even dimensioned like 2x2,4x4 are not considered is due their asymmetry property during matrix multiplication causes aliasing
     errors or loss of pixel information.

How many times do we need to perform 3x3 convolution operation to reach 1x1 

199*199| (3x3) Layer1 |197*197 |(3x3) Layer2 | 195*195 |(3x3) Layer3 | 193*193 |(3x3) Layer4 | 191*191 |(3x3) Layer5 |
189*189 | (3x3) Layer6 |187*187 | (3x3) Layer7 |185*185 | (3x3) Layer8 |183*183 |(3x3) Layer9 | 181*181 | (3x3) Layer10 |
179*179 |(3x3) Layer11 | 177*177 |(3x3) Layer12 | 175*175 |(3x3) Layer13 | 173*173 |(3x3) Layer14 | 171*171 | (3x3) Layer15 |
169*169 |(3x3) Layer16 | 167*167 |(3x3) Layer17 | 165*165 | (3x3) Layer18 |163*163 |(3x3) Layer19 | 161*161 | (3x3) Layer20 |
159*159 |(3x3) Layer21 | 157*157 |(3x3) Layer22 | 155*155 | (3x3) Layer23 |153*153 | (3x3) Layer24 |151*151 | (3x3) Layer25 |
149*149 | (3x3) Layer26 |147*147 | (3x3) Layer27 |145*145 |(3x3) Layer28 | 143*143 |(3x3) Layer29 | 141*141 | (3x3) Layer30 |
139*139 |(3x3) Layer31 | 137*137 | (3x3) Layer32 |135*135 |(3x3) Layer33 | 133*133 |(3x3) Layer34 | 131*131 | (3x3) Layer35 |
129*129 | (3x3) Layer36 |127*127 |(3x3) Layer37 | 125*125 | (3x3) Layer38 |123*123| (3x3) Layer39 |121*121 | (3x3) Layer40 |
119*119 | (3x3) Layer41 |117*117 | (3x3) Layer42 |115*115 | (3x3) Layer43 |113*113 |(3x3) Layer44 | 111*111 |(3x3) Layer45 |
109*109 |(3x3) Layer46 | 107*107 | (3x3) Layer47 |105*105 |(3x3) Layer48 | 103*103 |(3x3) Layer49 | 101*101 | (3x3) Layer50 |
99*99 |(3x3) Layer51 | 97*97 |(3x3) Layer52 | 95*95 |(3x3) Layer53 | 93*93 |(3x3) Layer54 | 91*91 |(3x3) Layer55 |
89*89 |(3x3) Layer56 | 87*87 | (3x3) Layer57 |85*85 | (3x3) Layer58 |83*83 | (3x3) Layer59 |81*81 | (3x3) Layer60 |
79*79 | (3x3) Layer61 |77*77 | (3x3) Layer62 |75*75 |(3x3) Layer63 |72*72 | (3x3) Layer64 |69*69 | (3x3) Layer65 |
67*67 | (3x3) Layer66 |65*65 |(3x3) Layer67 | 63*63 |(3x3) Layer68 | 62*62 | (3x3) Layer69 |61*61 | (3x3) Layer70 |
59*59 |3x3) Layer71 | 57*57 | 3x3) Layer72 |55*55 |3x3) Layer73 | 53*53 |3x3) Layer74 | 51*51 | 3x3) Layer75 |
49*49 | 3x3) Layer76 |47*47 |3x3) Layer77 | 45*45 | 3x3) Layer78 |43*43 | 3x3) Layer79 |42*42 | (3x3) Layer80 |
41*41 |(3x3) Layer81 | 39*39 |(3x3) Layer82 | 37*37 |(3x3) Layer83 | 35*35 |(3x3) Layer84 | 33*33 |(3x3) Layer85 |
31*31 |(3x3) Layer86 | 29*29 |(3x3) Layer87 | 27*27 | (3x3) Layer88 |25*25 | (3x3) Layer89 |(3x3) Layer90 |
23*23 |(3x3) Layer91 | 21*21 |(3x3) Layer92 | 19*19 | (3x3) Layer93 |17*17 | (3x3) Layer94 |15*15 |(3x3) Layer95 |
13*13 |(3x3) Layer96 | 11*11 |(3x3) Layer97 | 9*9 | (3x3) Layer98 |7*7 | (3x3) Layer99 |5*5 |(3x3) Layer100 | 3*3 |
|1*1
