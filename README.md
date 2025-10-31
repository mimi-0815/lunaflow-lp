     1	<!DOCTYPE html>
     2	<html lang="ja">
     3	<head>
     4	    <meta charset="UTF-8">
     5	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
     6	    <title>LunaFlow | 業界初！仕入れ代行付きサブスク物販スクール</title>
     7	    <style>
     8	        * {
     9	            margin: 0;
    10	            padding: 0;
    11	            box-sizing: border-box;
    12	        }
    13	        
    14	        body {
    15	            font-family: 'Helvetica Neue', 'Arial', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', 'Meiryo', sans-serif;
    16	            line-height: 1.6;
    17	            color: #333;
    18	            background: linear-gradient(135deg, #f5f3f0 0%, #e8ddd4 100%);
    19	        }
    20	        
    21	        .container {
    22	            max-width: 1200px;
    23	            margin: 0 auto;
    24	            padding: 0 20px;
    25	        }
    26	        
    27	        /* ヘッダー */
    28	        .header {
    29	            background: linear-gradient(135deg, #d4a574 0%, #b8956f 100%);
    30	            color: white;
    31	            padding: 60px 0;
    32	            text-align: center;
    33	            position: relative;
    34	            overflow: hidden;
    35	        }
    36	        
    37	        .header::before {
    38	            content: '';
    39	            position: absolute;
    40	            top: -50%;
    41	            left: -50%;
    42	            width: 200%;
    43	            height: 200%;
    44	            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
    45	            background-size: 30px 30px;
    46	            animation: sparkle 20s linear infinite;
    47	        }
    48	        
    49	        @keyframes sparkle {
    50	            0% { transform: translate(0, 0) rotate(0deg); }
    51	            100% { transform: translate(-30px, -30px) rotate(360deg); }
    52	        }
    53	        
    54	        .header-content {
    55	            position: relative;
    56	            z-index: 2;
    57	        }
    58	        
    59	        .header h1 {
    60	            font-size: 3.5rem;
    61	            font-weight: bold;
    62	            margin-bottom: 20px;
    63	            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    64	        }
    65	        
    66	        .header .subtitle {
    67	            font-size: 1.8rem;
    68	            margin-bottom: 30px;
    69	            opacity: 0.9;
    70	        }
    71	        
    72	        .header .highlight {
    73	            background: rgba(255,255,255,0.2);
    74	            padding: 15px 30px;
    75	            border-radius: 50px;
    76	            display: inline-block;
    77	            font-size: 1.4rem;
    78	            font-weight: bold;
    79	            margin-top: 20px;
    80	        }
    81	        
    82	        /* 3つの不安解消セクション */
    83	        .problems {
    84	            padding: 80px 0;
    85	            background: white;
    86	        }
    87	        
    88	        .problems h2 {
    89	            text-align: center;
    90	            font-size: 2.5rem;
    91	            margin-bottom: 60px;
    92	            color: #b8956f;
    93	        }
    94	        
    95	        .problem-grid {
    96	            display: grid;
    97	            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    98	            gap: 40px;
    99	            margin-bottom: 60px;
   100	        }
   101	        
   102	        .problem-card {
   103	            text-align: center;
   104	            padding: 40px 20px;
   105	            border-radius: 20px;
   106	            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
   107	            transition: transform 0.3s ease;
   108	        }
   109	        
   110	        .problem-card:hover {
   111	            transform: translateY(-10px);
   112	        }
   113	        
   114	        .problem-card.problem {
   115	            background: linear-gradient(135deg, #ffe4e4 0%, #ffcccc 100%);
   116	        }
   117	        
   118	        .problem-card.solution {
   119	            background: linear-gradient(135deg, #e4f7ff 0%, #ccedff 100%);
   120	        }
   121	        
   122	        .problem-icon {
   123	            font-size: 4rem;
   124	            margin-bottom: 20px;
   125	            display: block;
   126	        }
   127	        
   128	        .problem-card h3 {
   129	            font-size: 1.8rem;
   130	            margin-bottom: 20px;
   131	        }
   132	        
   133	        .problem-card p {
   134	            font-size: 1.1rem;
   135	            line-height: 1.8;
   136	        }
   137	        
   138	        /* 料金プラン */
   139	        .pricing {
   140	            padding: 80px 0;
   141	            background: linear-gradient(135deg, #f8f6f3 0%, #ede8e0 100%);
   142	        }
   143	        
   144	        .pricing h2 {
   145	            text-align: center;
   146	            font-size: 2.5rem;
   147	            margin-bottom: 60px;
   148	            color: #b8956f;
   149	        }
   150	        
   151	        .pricing-grid {
   152	            display: grid;
   153	            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
   154	            gap: 30px;
   155	        }
   156	        
   157	        .pricing-card {
   158	            background: white;
   159	            border-radius: 20px;
   160	            padding: 40px 30px;
   161	            text-align: center;
   162	            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
   163	            position: relative;
   164	            transition: transform 0.3s ease;
   165	        }
   166	        
   167	        .pricing-card:hover {
   168	            transform: translateY(-15px);
   169	        }
   170	        
   171	        .pricing-card.featured {
   172	            transform: scale(1.05);
   173	            border: 3px solid #d4a574;
   174	        }
   175	        
   176	        .pricing-card.featured::before {
   177	            content: '人気No.1';
   178	            position: absolute;
   179	            top: -15px;
   180	            left: 50%;
   181	            transform: translateX(-50%);
   182	            background: #d4a574;
   183	            color: white;
   184	            padding: 8px 25px;
   185	            border-radius: 25px;
   186	            font-weight: bold;
   187	        }
   188	        
   189	        .pricing-card h3 {
   190	            font-size: 2rem;
   191	            margin-bottom: 10px;
   192	            color: #b8956f;
   193	        }
   194	        
   195	        .pricing-card .price {
   196	            font-size: 3rem;
   197	            font-weight: bold;
   198	            color: #d4a574;
   199	            margin-bottom: 5px;
   200	        }
   201	        
   202	        .pricing-card .period {
   203	            color: #666;
   204	            margin-bottom: 30px;
   205	        }
   206	        
   207	        .pricing-card .feature {
   208	            margin-bottom: 15px;
   209	            padding: 10px 0;
   210	            border-bottom: 1px solid #eee;
   211	        }
   212	        
   213	        .pricing-card .feature:last-child {
   214	            border-bottom: none;
   215	        }
   216	        
   217	        .pricing-card .cta {
   218	            background: linear-gradient(135deg, #d4a574 0%, #b8956f 100%);
   219	            color: white;
   220	            padding: 15px 30px;
   221	            border-radius: 50px;
   222	            text-decoration: none;
   223	            font-weight: bold;
   224	            font-size: 1.2rem;
   225	            display: inline-block;
   226	            margin-top: 20px;
   227	            transition: all 0.3s ease;
   228	        }
   229	        
   230	        .pricing-card .cta:hover {
   231	            transform: translateY(-3px);
   232	            box-shadow: 0 10px 25px rgba(212, 165, 116, 0.4);
   233	        }
   234	        
   235	        .pricing-card .terms-notice {
   236	            font-size: 0.7rem;
   237	            color: #999;
   238	            margin-top: 15px;
   239	            line-height: 1.4;
   240	        }
   241	        
   242	        .pricing-card .terms-notice a {
   243	            color: #d4a574;
   244	            text-decoration: underline;
   245	        }
   246	        
   247	        .pricing-card .terms-notice a:hover {
   248	            color: #b8956f;
   249	        }
   250	        
   251	        /* 契約条件セクション */
   252	        .contract-terms {
   253	            background: #fff8e1;
   254	            border: 2px solid #ffd54f;
   255	            padding: 30px;
   256	            border-radius: 15px;
   257	            margin: 40px auto;
   258	            max-width: 900px;
   259	        }
   260	        
   261	        .contract-terms h3 {
   262	            color: #f57c00;
   263	            margin-bottom: 20px;
   264	            font-size: 1.5rem;
   265	        }
   266	        
   267	        .contract-terms ul {
   268	            list-style: none;
   269	            padding: 0;
   270	        }
   271	        
   272	        .contract-terms li {
   273	            padding: 10px 0;
   274	            padding-left: 25px;
   275	            position: relative;
   276	        }
   277	        
   278	        .contract-terms li::before {
   279	            content: '✓';
   280	            position: absolute;
   281	            left: 0;
   282	            color: #4caf50;
   283	            font-weight: bold;
   284	        }
   285	        
   286	        .contract-terms .important {
   287	            background: white;
   288	            padding: 15px;
   289	            border-radius: 10px;
   290	            margin-top: 20px;
   291	            border-left: 4px solid #f57c00;
   292	        }
   293	        
   294	        /* 特別オファー */
   295	        .offer {
   296	            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
   297	            color: white;
   298	            padding: 60px 0;
   299	            text-align: center;
   300	        }
   301	        
   302	        .offer h2 {
   303	            font-size: 2.5rem;
   304	            margin-bottom: 20px;
   305	        }
   306	        
   307	        .offer p {
   308	            font-size: 1.4rem;
   309	            margin-bottom: 30px;
   310	        }
   311	        
   312	        .offer .timer {
   313	            font-size: 2rem;
   314	            font-weight: bold;
   315	            background: rgba(255,255,255,0.2);
   316	            padding: 20px;
   317	            border-radius: 15px;
   318	            display: inline-block;
   319	        }
   320	        
   321	        /* FAQ */
   322	        .faq {
   323	            padding: 80px 0;
   324	            background: white;
   325	        }
   326	        
   327	        .faq h2 {
   328	            text-align: center;
   329	            font-size: 2.5rem;
   330	            margin-bottom: 60px;
   331	            color: #b8956f;
   332	        }
   333	        
   334	        .faq-item {
   335	            margin-bottom: 30px;
   336	            border: 1px solid #eee;
   337	            border-radius: 10px;
   338	            overflow: hidden;
   339	        }
   340	        
   341	        .faq-question {
   342	            background: #f8f6f3;
   343	            padding: 20px;
   344	            font-weight: bold;
   345	            font-size: 1.2rem;
   346	            cursor: pointer;
   347	            transition: background-color 0.3s ease;
   348	        }
   349	        
   350	        .faq-question:hover {
   351	            background: #ede8e0;
   352	        }
   353	        
   354	        .faq-answer {
   355	            padding: 20px;
   356	            display: none;
   357	            line-height: 1.8;
   358	        }
   359	        
   360	        /* フッター */
   361	        .footer {
   362	            background: #333;
   363	            color: white;
   364	            padding: 40px 0;
   365	            text-align: center;
   366	        }
   367	        
   368	        .footer a {
   369	            color: #d4a574;
   370	            text-decoration: none;
   371	            margin: 0 15px;
   372	        }
   373	        
   374	        .footer a:hover {
   375	            text-decoration: underline;
   376	        }
   377	        
   378	        /* レスポンシブ */
   379	        @media (max-width: 768px) {
   380	            .header h1 {
   381	                font-size: 2.5rem;
   382	            }
   383	            
   384	            .header .subtitle {
   385	                font-size: 1.4rem;
   386	            }
   387	            
   388	            .pricing-grid {
   389	                grid-template-columns: 1fr;
   390	            }
   391	            
   392	            .pricing-card.featured {
   393	                transform: none;
   394	            }
   395	        }
   396	    </style>
   397	</head>
   398	<body>
   399	    <!-- ヘッダー -->
   400	    <section class="header">
   401	        <div class="container">
   402	            <div class="header-content">
   403	                <h1>LunaFlow</h1>
   404	                <p class="subtitle">業界初！仕入れ代行付きサブスク物販スクール</p>
   405	                <div class="highlight">
   406	                    初期費用0円、月額5,980円から始める新しい物販教育
   407	                </div>
   408	            </div>
   409	        </div>
   410	    </section>
   411	
   412	    <!-- 3つの不安解消 -->
   413	    <section class="problems">
   414	        <div class="container">
   415	            <h2>こんなお悩みありませんか？</h2>
   416	            
   417	            <div class="problem-grid">
   418	                <div class="problem-card problem">
   419	                    <span class="problem-icon">❌</span>
   420	                    <h3>高額スクールで失敗したくない</h3>
   421	                    <p>「40万円払ったのに結果が出なかった...」<br>
   422	                    そんな話をよく聞きます。高額な初期費用は心理的な負担が大きすぎます。</p>
   423	                </div>
   424	                
   425	                <div class="problem-card problem">
   426	                    <span class="problem-icon">❌</span>
   427	                    <h3>仕入れ資金がない</h3>
   428	                    <p>「勉強したけど仕入れる資金がない...」<br>
   429	                    知識だけもらっても、実際に商品を仕入れられなければ意味がありません。</p>
   430	                </div>
   431	                
   432	                <div class="problem-card problem">
   433	                    <span class="problem-icon">❌</span>
   434	                    <h3>何から始めればいいかわからない</h3>
   435	                    <p>「物販って難しそう...」<br>
   436	                    初心者が一人で始めるには、ハードルが高すぎるのが現実です。</p>
   437	                </div>
   438	            </div>
   439	            
   440	            <h2 style="color: #d4a574; margin-top: 60px;">LunaFlowが全て解決します！</h2>
   441	            
   442	            <div class="problem-grid">
   443	                <div class="problem-card solution">
   444	                    <span class="problem-icon">✅</span>
   445	                    <h3>月額制でリスクゼロ</h3>
   446	                    <p>最低契約期間1年、中途解約も可能！<br>
   447	                    高額な初期費用は一切不要。まずは月5,980円から始められます。</p>
   448	                </div>
   449	                
   450	                <div class="problem-card solution">
   451	                    <span class="problem-icon">✅</span>
   452	                    <h3>最大8万円の仕入れ代行</h3>
   453	                    <p>あなたに代わって商品を仕入れします！<br>
   454	                    資金がなくても、運営が立て替えて仕入れ。売上から回収するので安心です。</p>
   455	                </div>
   456	                
   457	                <div class="problem-card solution">
   458	                    <span class="problem-icon">✅</span>
   459	                    <h3>30本の動画で完全ガイド</h3>
   460	                    <p>初心者でも迷わない！<br>
   461	                    登録から初売上まで、全てを動画で解説。Discord内で質問し放題です。</p>
   462	                </div>
   463	            </div>
   464	        </div>
   465	    </section>
   466	
   467	    <!-- 料金プラン -->
   468	    <section class="pricing">
   469	        <div class="container">
   470	            <h2>選べる3つのプラン</h2>
   471	            
   472	            <!-- 契約条件の明記 -->
   473	            <div class="contract-terms">
   474	                <h3>⚠️ 契約条件について</h3>
   475	                <ul>
   476	                    <li><strong>最低契約期間：1年間（12ヶ月）</strong></li>
   477	                    <li>1年経過後はいつでも解約可能（手数料なし）</li>
   478	                    <li>1年以内の中途解約も可能ですが、手数料が発生します</li>
   479	                </ul>
   480	                <div class="important">
   481	                    <strong>中途解約手数料：</strong><br>
   482	                    ・6ヶ月未満：残期間の月額料金 × 50%<br>
   483	                    ・6ヶ月以上：残期間の月額料金 × 25%<br>
   484	                    <a href="riyoukiyaku.html" target="_blank" style="color: #d4a574;">詳細は利用規約をご確認ください</a>
   485	                </div>
   486	            </div>
   487	            
   488	            <div class="pricing-grid">
   489	                <div class="pricing-card">
   490	                    <h3>Light</h3>
   491	                    <div class="price">¥5,980</div>
   492	                    <div class="period">/ 月額</div>
   493	                    <div class="feature"><strong>必須仕入れ：¥80,000以上</strong></div>
   494	                    <div class="feature">基礎動画20本見放題</div>
   495	                    <div class="feature">Discord質問チャンネル利用</div>
   496	                    <div class="feature">仕入れ代行サービス</div>
   497	                    <div class="feature">LINE個別サポート</div>
   498	                    <div class="feature">紹介プログラム参加</div>
   499	                    <a href="https://buy.stripe.com/00wdR90j8fprfVo7pjc7u01" class="cta">Lightプランで始める</a>
   500	                    <div class="terms-notice">
   501	                        ※最低契約期間1年、中途解約可能（手数料あり）<br>
   502	                        <a href="riyoukiyaku.html" target="_blank">利用規約</a> | 
   503	                        <a href="tokusho.html" target="_blank">特定商取引法</a>
   504	                    </div>
   505	                </div>
   506	                
   507	                <div class="pricing-card featured">
   508	                    <h3>Standard</h3>
   509	                    <div class="price">¥12,980</div>
   510	                    <div class="period">/ 月額</div>
   511	                    <div class="feature"><strong>必須仕入れ：¥50,000以上</strong></div>
   512	                    <div class="feature">全30本の動画見放題</div>
   513	                    <div class="feature"><strong>中古リペア講座付き</strong></div>
   514	                    <div class="feature">リアル勉強会参加（¥5,000）</div>
   515	                    <div class="feature">優先サポート</div>
   516	                    <div class="feature">月1回グループコンサル</div>
   517	                    <a href="https://buy.stripe.com/9B6aEXc1Q6SVbF810Vc7u02" class="cta">Standardプランで始める</a>
   518	                    <div class="terms-notice">
   519	                        ※最低契約期間1年、中途解約可能（手数料あり）<br>
   520	                        <a href="riyoukiyaku.html" target="_blank">利用規約</a> | 
   521	                        <a href="tokusho.html" target="_blank">特定商取引法</a>
   522	                    </div>
   523	                </div>
   524	                
   525	                <div class="pricing-card">
   526	                    <h3>Premium</h3>
   527	                    <div class="price">¥19,800</div>
   528	                    <div class="period">/ 月額</div>
   529	                    <div class="feature"><strong>必須仕入れ：¥30,000以上</strong></div>
   530	                    <div class="feature">全コンテンツ無制限</div>
   531	                    <div class="feature">中古リペア講座付き</div>
   532	                    <div class="feature"><strong>リアル勉強会無料参加</strong></div>
   533	                    <div class="feature">個別Zoom相談月2回</div>
   534	                    <div class="feature">最優先サポート</div>
   535	                    <a href="https://buy.stripe.com/eVqfZhd5UcdfeRkdNHc7u03" class="cta">Premiumプランで始める</a>
   536	                    <div class="terms-notice">
   537	                        ※最低契約期間1年、中途解約可能（手数料あり）<br>
   538	                        <a href="riyoukiyaku.html" target="_blank">利用規約</a> | 
   539	                        <a href="tokusho.html" target="_blank">特定商取引法</a>
   540	                    </div>
   541	                </div>
   542	            </div>
   543	        </div>
   544	    </section>
   545	
   546	    <!-- 特別オファー -->
   547	    <section class="offer">
   548	        <div class="container">
   549	            <h2>🎉 ローンチ記念特別オファー 🎉</h2>
   550	            <p>先着30名様限定！入会金¥10,000が今だけ</p>
   551	            <div class="timer">完全無料！</div>
   552	            <p style="margin-top: 20px;">※このオファーは予告なく終了する場合があります</p>
   553	        </div>
   554	    </section>
   555	
   556	    <!-- FAQ -->
   557	    <section class="faq">
   558	        <div class="container">
   559	            <h2>よくある質問</h2>
   560	            
   561	            <div class="faq-item">
   562	                <div class="faq-question" onclick="toggleFaq(this)">
   563	                    Q. 本当に月額料金だけで大丈夫ですか？
   564	                </div>
   565	                <div class="faq-answer">
   566	                    A. はい、隠れた費用は一切ありません。表示されている月額料金のみです。ただし、商品の仕入れ代金は売上から回収させていただきます。
   567	                </div>
   568	            </div>
   569	            
   570	            <div class="faq-item">
   571	                <div class="faq-question" onclick="toggleFaq(this)">
   572	                    Q. 最低契約期間1年は厳しいですか？
   573	                </div>
   574	                <div class="faq-answer">
   575	                    A. 1年間は物販で安定した収益を得るために必要な期間です。ただし、やむを得ない事情で解約される場合は、中途解約手数料をお支払いいただくことで解約可能です。詳細は<a href="riyoukiyaku.html" target="_blank" style="color: #d4a574;">利用規約</a>をご確認ください。
   576	                </div>
   577	            </div>
   578	            
   579	            <div class="faq-item">
   580	                <div class="faq-question" onclick="toggleFaq(this)">
   581	                    Q. 仕入れ代行の仕組みはどうなっていますか？
   582	                </div>
   583	                <div class="faq-answer">
   584	                    A. 運営が商品を選定・仕入れし、あなたのアカウントで販売していただきます。売上が出た時点で仕入れ代金＋手数���を差し引いた利益をお渡しします。
   585	                </div>
   586	            </div>
   587	            
   588	            <div class="faq-item">
   589	                <div class="faq-question" onclick="toggleFaq(this)">
   590	                    Q. 初心者でも本当に稼げますか？
   591	                </div>
   592	                <div class="faq-answer">
   593	                    A. はい。仕入れから販売まで全面的にサポートします。また、30本の動画教材で基礎から学べるため、未経験の方でも安心して始められます。
   594	                </div>
   595	            </div>
   596	            
   597	            <div class="faq-item">
   598	                <div class="faq-question" onclick="toggleFaq(this)">
   599	                    Q. 返金保証はありますか？
   600	                </div>
   601	                <div class="faq-answer">
   602	                    A. 入会後7日以内であれば全額返金いたします。ただし、Discord教材の視聴は5本まで、仕入れ代行未利用の場合に限ります。
   603	                </div>
   604	            </div>
   605	        </div>
   606	    </section>
   607	
   608	    <!-- フッター -->
   609	    <footer class="footer">
   610	        <div class="container">
   611	            <p>&copy; 2024 LunaFlow. All rights reserved.</p>
   612	            <div style="margin-top: 20px;">
   613	                <a href="tokusho.html">特定商取引法に基づく表記</a>
   614	                <a href="privacy.html">プライバシーポリシー</a>
   615	                <a href="riyoukiyaku.html">利用規約</a>
   616	            </div>
   617	        </div>
   618	    </footer>
   619	
   620	    <script>
   621	        function toggleFaq(element) {
   622	            const answer = element.nextElementSibling;
   623	            const isOpen = answer.style.display === 'block';
   624	            
   625	            // 全てのFAQを閉じる
   626	            document.querySelectorAll('.faq-answer').forEach(item => {
   627	                item.style.display = 'none';
   628	            });
   629	            
   630	            // クリックされたFAQを開く/閉じる
   631	            if (!isOpen) {
   632	                answer.style.display = 'block';
   633	            }
   634	        }
   635	        
   636	        // スムーススクロール
   637	        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
   638	            anchor.addEventListener('click', function (e) {
   639	                e.preventDefault();
   640	                const target = document.querySelector(this.getAttribute('href'));
   641	                if (target) {
   642	                    target.scrollIntoView({
   643	                        behavior: 'smooth'
   644	                    });
   645	                }
   646	            });
   647	        });
   648	    </script>
   649	</body>
   650	</html>
