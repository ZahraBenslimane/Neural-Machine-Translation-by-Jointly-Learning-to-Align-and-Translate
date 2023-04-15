# Neural Machine Translation by Jointly Learning to Align and Translate
Neural machine translation is a recently proposed approach to machine translation. Unlike the traditional statistical machine translation, the neural machine translation aims at building a single neural network that can be jointly tuned to maximize the translation performance.


\documentclass{article}
\usepackage{amsmath}
\usepackage{color,pxfonts,fix-cm}
\usepackage{latexsym}
\usepackage[mathletters]{ucs}
\DeclareUnicodeCharacter{8211}{\textendash}
\DeclareUnicodeCharacter{34}{\textquotedbl}
\DeclareUnicodeCharacter{46}{\textperiodcentered}
\DeclareUnicodeCharacter{8242}{$\prime$}
\DeclareUnicodeCharacter{58}{$\colon$}
\DeclareUnicodeCharacter{8216}{\textquoteleft}
\DeclareUnicodeCharacter{945}{$\alpha$}
\DeclareUnicodeCharacter{60}{\textless}
\DeclareUnicodeCharacter{8592}{$\leftarrow$}
\DeclareUnicodeCharacter{62}{\textgreater}
\usepackage[T1]{fontenc}
\usepackage[utf8x]{inputenc}
\usepackage{pict2e}
\usepackage{wasysym}
\usepackage[english]{babel}
\usepackage{tikz}
\pagestyle{empty}
\usepackage[margin=0in,paperwidth=612pt,paperheight=792pt]{geometry}
\begin{document}
\definecolor{color_29791}{rgb}{0,0,0}
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(88.398,-100.787){\fontsize{14.3462}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}Neural Mac hine T ranslation b y Join tly Learning to Align}
\put(242.611,-118.72){\fontsize{14.3462}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}and T ranslate}
\put(75,-147.838){\fontsize{9.9626}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}BENAISSA T arek, BENBRAHIM Mohammed El Amine, BENSLIMANE Zahra Ha-}
\put(75,-159.793){\fontsize{9.9626}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}fida, BENABID M’hamed Djahid}
\put(75,-193.349){\fontsize{8.9664}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}Editor: Mac hine Learning Av anc ´ e (2021-2022)}
\put(265.298,-229.146){\fontsize{11.9552}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}Abstract}
\put(94.925,-243.107){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}As a part of Adv anced Mac hine Learning pro ject w e re-implemen ted a neural mac hine translation,}
\put(94.925,-254.066){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The pap er in tro duced a mo del that translates one sen tence from a source language in to a se n tence}
\put(94.925,-265.025){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}in a target language.}
\put(109.869,-275.9839){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}This mo del consists of 3 ma jor parts, an enco der,reads the input sen tence and enco des it in to}
\put(94.925,-286.9429){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}a seque nce of v ectors of v ariable length, and a deco der that outputs a sequence of w ord probabilit y}
\put(94.925,-297.9019){\fontsize{8.9664}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}v e ctors in the target language and atten tion ...}
\put(75,-329.1299){\fontsize{11.9552}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}1. In tro duction}
\put(89.944,-348.2849){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Neural mac hine translation is task that’s b ecoming more and more esse n tial for man y indus-}
\put(75,-360.2399){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}tries of to d a y’s w orld. The o v erwhelming ma jorit y of the neural mac hine translation mo dels are}
\put(75,-372.1959){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}of the enco der-deco der t yp e. Our role in this pro ject is to rev erse engineer the results obtained in}
\put(75,-384.1509){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the pap er ”NEURAL MA CHINE TRANSLA TION BY JOINTL Y LEARNING TO ALIGN AND}
\put(75,-396.1059){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}TRANSLA TE” b y Bahdanau, Cho and Bengio. The pap er in tro duces an inno v ation to the classic}
\put(75,-408.0609){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}enco der-deco der mo del b y learning to align and translate join tly .}
\put(75,-439.2888){\fontsize{11.9552}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}2. Neural Mac hine T ra ns la tion}
\put(89.944,-458.4449){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The global arc hitecture of the mo del prop osed b y the pap er consists of 3 main parts. the enco der,}
\put(75,-470.3998){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the atten tion mo del and the d e co der. the graphical illustration of the mo del is sho wn b elo w :}
\put(288.509,-722.7499){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1}
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(163.441,-314.507){\includegraphics[width=255.132pt,height=233.6472pt]{latexImage_367337eea4a8ab666e944a9788052eb6.png}}
\put(147.586,-332.838){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Figure 1 – Neural Mac hine T ranslation with atten tion o v erview}
\put(75,-362.78){\fontsize{9.9626}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}2.1 Enco der}
\put(89.944,-380.495){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The enco der is a recursiv e neural net w ork (RNN) that reads an input s equ e n c e x starting fr o m}
\put(75,-392.45){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the first w ord to the last one. Ho w ev er, in our mo d e l w e ha v e used a Bidirectional RNN whic h are}
\put(75,-404.405){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}t w o RNNs one running forw ard o v er th e input sequence and the other running bac kw ard whic h lead}
\put(75,-416.361){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}to output t w o hidden state s for eac h input, the forw ard hidd e n state con tain information from earlier}
\put(75,-428.3159){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}in the sequence and the b ac kw ard from later in the sequence, b y concatenating the t w o hidden states}
\put(75,-440.2709){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}it results an annotation h}
\put(186.593,-441.7649){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(194.112,-440.2709){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}for eac h w ord.}
\put(75,-452.2259){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the annotation i s expressed b y :}
\put(261.516,-472.5939){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(267.256,-474.0889){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(274.221,-472.5939){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(284.737,-455.5579){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}"}
\put(296.978,-463.4749){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}⃗}
\put(297.642,-466.1039){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(303.382,-467.5979){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(295.53,-473.3449){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}← −}
\put(297.642,-480.2639){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(305.493,-481.7579){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(314.672,-455.5579){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}\#}
\put(74.99997,-503.9769){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Where the forw ard hidden state is giv en b y :}
\put(197.406,-531.7339){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}⃗}
\put(198.07,-534.3629){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(203.81,-535.8569){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(210.775,-534.3629){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(221.291,-517.3269){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}(}
\put(229.316,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}(1 − ⃗ z}
\put(254.982,-529.0629){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(259.18,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}) ◦}
\put(271.799,-524.9389){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}⃗}
\put(272.463,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(278.203,-529.0629){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j − 1}
\put(294.813,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}+ ⃗ z}
\put(309.408,-529.0629){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(315.82,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}◦}
\put(322.352,-524.9389){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}⃗}
\put(323.015,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(328.755,-529.0629){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(342.916,-527.5679){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}, if j > 0}
\put(229.316,-541.9149){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}0 , if j = 0}
\put(74.99997,-565.7449){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the annotation will b e used for align m en t and the deco der later.}
\put(74.99997,-592.0999){\fontsize{9.9626}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}2.2 A tten tion}
\put(89.94397,-609.8159){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}One of the problems in mac hine tran s lati on is Alignmen t b ecause i t iden tifies whic h part of the}
\put(74.99997,-621.7709){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}input sequence can matc h with e ac h w ord in the output, so Bahdanau atten tion is prop osed, it is an}
\put(74.99997,-633.7259){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}in terface b et w een the enco d e r and deco der that pro vides the deco der with information from ev ery}
\put(74.99997,-645.6809){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}enco der hidden state. With this setting, the mo del is able to selec ti v ely fo cus on useful par ts of the}
\put(74.99997,-657.6359){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}input sequence and hence, learn the alignmen t b et w e en them. A s explained in the previous section,}
\put(74.99997,-669.5919){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the annotations th at w ere made b y the enco der are used to computed the con text v ector c}
\put(465.699,-671.0859){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}i}
\put(472.068,-669.5919){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}whic h is}
\put(288.509,-722.7499){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2}
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75,-90.82397){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}a w eigh ted sum of the annotations h}
\put(234.442,-92.31897){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}i}
\put(241.079,-90.82397){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}and is giv en b y :}
\put(260.855,-122.046){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}c}
\put(265.166,-123.541){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}i}
\put(271.25,-122.046){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(284.388,-109.4819){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}T}
\put(289.094,-110.4779){\fontsize{4.9813}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}x}
\put(281.767,-112.5819){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}X}
\put(282.068,-133.8009){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j =1}
\put(297.817,-122.0459){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}α}
\put(304.191,-123.5409){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(311.207,-122.0459){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}h}
\put(316.947,-123.5409){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(75.00002,-154.0309){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The w eigh t a}
\put(132.293,-155.5249){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(142.631,-154.0309){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}of eac h hidden state h}
\put(239.197,-155.5249){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(243.395,-154.0309){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}, whic h is call atten tion w eigh t , is com p uted b y}
\put(244.391,-182.0519){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}α}
\put(250.764,-183.5459){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(260.548,-182.0519){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(286.194,-175.3119){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}exp ( e}
\put(311.588,-176.8059){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(318.605,-175.3119){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791})}
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\draw[color_29791,line width=0.398pt]
(272.259pt, -179.561pt) -- (336.414pt, -179.561pt)
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(272.259,-183.258){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}P}
\put(282.775,-185.721){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}T}
\put(287.481,-186.717){\fontsize{4.9813}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}x}
\put(282.775,-193.719){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}k =1}
\put(299.425,-190.73){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}exp ( e}
\put(324.819,-192.225){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ik}
\put(332.54,-190.73){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791})}
\put(75,-211.596){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}e}
\put(79.639,-213.091){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(89.976,-211.596){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}is the alignmen t where :}
\put(254.346,-223.552){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}e}
\put(258.985,-225.046){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}ij}
\put(268.769,-223.552){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}= α ( s}
\put(295.899,-225.046){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}i − 1}
\put(309.414,-223.552){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}, h}
\put(319.582,-225.046){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}j}
\put(323.78,-223.552){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791})}
\put(75,-241.484){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}W e can in terpret the v alues of α as it tell us h o w m uc h atten tion the mo del should pa y to the w or d}
\put(75,-253.44){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}in the inpu t when generating a certain output.}
\put(75,-279.794){\fontsize{9.9626}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}2.3 Deco der}
\put(89.944,-297.51){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The con text v ector that is ob tained in the previous step is concatenated with the previous deco der}
\put(75,-309.465){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}output and fed in to the Deco der RNN cell to pro duce a new hidden state. Then,the p ro cess rep eats}
\put(75,-321.42){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}itself for eac h time step of the deco der un til an ‘ < end >}
\put(340.254,-317.805){\fontsize{6.9738}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_29791}′}
\put(347.344,-321.42){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}tok en is pro duced or output is past}
\put(75,-333.375){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the sp ecified maxim u m length. The final outp ut for the time step is obtained b y passing th e new}
\put(75,-345.33){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}hidden state through a Linear la y er, whic h acts as a classifier to giv e the probabilit y s cores of the}
\put(75,-357.2859){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}next predicted w ord.}
\put(75,-388.5139){\fontsize{11.9552}{1}\usefont{T1}{cmr}{b}{n}\selectfont\color{color_29791}3. D atasets}
\put(89.944,-407.6689){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The WMT’ 14 dataset con tains appro ximately 850M w ords, during our researc h the time needed}
\put(75,-419.6239){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}for our mo del to train on the totallit y of th e dataset w ould b e closer to 6 da ys . Eviden tly , w e c h os e to}
\put(75,-431.5799){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}shrink the dataset to a couple h undred thousand w ords, to facilitate the pro cess an d mak e sure our}
\put(75,-443.5349){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}p ython co de w as c or re ct b efore mo ving in to the full dataset. W e c hose to concatenate the Europarl}
\put(75,-455.4899){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}dataset with the IWSL T-17 dataset to form our mini-set}
\put(288.509,-722.7499){\fontsize{9.9626}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}3}
\end{picture}
\end{document}
