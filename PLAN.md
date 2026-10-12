# kanatogglbilehtmlkanaview - 히라가나랑 가타가나를 둘다 못 외우는 인간들을 위한 [htmlkanaview](https://github.com/FarAway6834/htmlkanaview)

파일 : [kanatogglbilehtmlkanaview.py](https://github.com/FarAway6834/blob/main/kanatogglbilehtmlkanaview.py)

걍 파일에 독스트링 좋으니까 읽어 ㅋㅋㅋㅋㅋ

크ㅏㅎ핳 설명 유기

## 주요 추가사항

customible_kanahint, kanahint를 통한
1. 히라가나의 가타가나 힌트 기능 (일본 어린이들중엔 가타가나만 읽는 케이스도 있다.)
2. 가타가나의 히라가나 힌트 기능 (그리고 나같은 머리나쁜 일본어 학습자같은 경우는 칼든 정신나간 부엉이 덕에 겨우겨우 히라가나를 익히기에, 히라가나밖에 모르는 경우도 있다.)

기본적으로, 커스터마이징된 문법을 쓸게 아니면, kanahint를 쓰길 권장한다. 그냥 모두 표준화되게 쓰면, 존나 폭력적이지ㄴㅏㅁ만, 편하잖아헿ㅎㅎㅎㅎ헿



그래서 kanahint가 어떻냐? 하면
 - `°°°°ka단스테가나나 가타가나°°°°`가 htmlkanaview_markup=True시 `[ka단스테가나나 가타가나](변환되엇기에 ka단스테가나나 히라가나)`, htmlkanaview_markup=False시 `ka단스테가나나 가타가나（변환되엇기에 ka단스테가나나 히라가나）`식으로
 - `°°°ka단스테가나나 히라가나°°°`가 htmlkanaview_markup=True시 `[ka단스테가나나 히라가나](변환되엇기에 ka단스테가나나 가타가나)`, htmlkanaview_markup=False시 `ka단스테가나나 히라가나（변환되엇기에 ka단스테가나나 가타가나）`식으로
 - `°°가타가나°°`가 htmlkanaview_markup=True시 `[가타가나](변환되엇기에 히라가나)`, htmlkanaview_markup=False시 `가타가나（변환되엇기에 히라가나）`식으로
 - `°히라가나°`가 htmlkanaview_markup=True시 `[히라가나](변환되엇기에 가타가나)`, htmlkanaview_markup=False시 `히라가나（변환되엇기에 가타가나）`식으로
변환해준다.

으헤헤 그러니까, htmlkanaview_markup가 참이면 바로 htmlkanaview로 넘겨서 쓸수 있는거라구 으헤헤

## htmlkanaview와 연동하기 위한 기능

pipelining_into_htmlkanaview라고 해서, pipelining_into_htmlkanaview(kanahint류 함수)식으로 넣어놓으면, pipelining_into_htmlkanaview가 compose(htmlkanaview, partial(inputed_function, htmlkanaview_markup = True))를 만들어주는거다. 이걸로, 이제 나도 노래할수있어

크악 ㅠㅠㅠㅠㅠㅠ

참고로, kanatogglbilehtmlkanaview란 함수는 이딴식으로 만들어진거다.

## 배포 후 기대

```python
>>> from kanatogglbilehtmlkanaview import kanatogglbilehtmlkanaview
>>> print("""\
[理解](りかい)できないな
その°°ヒステリック°°な[情緒](じょうちょ)
[動物](どうぶつ)みたいで
まだ[動](うご)けないな
[日和見](ひよりみ)の°°メッセージ°°
[化](ば)けた[迷路](めいろ)の[末](すえ)
[末端価格](まったんかかく)の°°アイラビュー°°
そのひとつで[世界](せかい)はこんなにも
ねぇ[絶賛何処](ぜっさんどこ)ぞの°°マリオネット]°°
[刻](きざ)まれた「[良](い)い[子](こ)」のA to Z
あたし[聖人君子](せいじんくんし)でありたいの
[中傷](ちゅうしょう)も[誹謗](ひぼう)も[真](ま)っ[平](ぴら)でさ
[製品価値](せいひんかち)だけ[頂戴](ちょうだい)な
[笑顔](えがお)は[解](と)けない
まだ[動](うご)けないまんま
°°フラ°°ついた°°ステップ°°
[踏](ふ)み[外](はず)さないように
ほら[全部全部](ぜんぶぜんぶ)が
[最適](さいてき)であるように\
""")
<ruby>り⃞⁣⁣か⃞⁣⁣い⃞<rp>（</rp><rt>理解</rt><rp）</rp></ruby>で⃞⁣⁣き⃞⁣⁣な⃞⁣⁣い⃞⁣⁣な⃞⁣⁣
⃞⁣⁣そ⃞⁣⁣の⃞<ruby>ひ⃞⁣⁣す⃞⁣⁣て⃞⁣⁣り⃞⁣⁣ ⃞⁣⁣っ⃞⁣⁣く⃞<rp>（</rp><rt>ヒステリック</rt><rp）</rp></ruby>な⃞<ruby>じ⃞⁣⁣ょ⃞⁣⁣う⃞⁣⁣ち⃞⁣⁣ょ⃞<rp>（</rp><rt>情緒</rt><rp）</rp></ruby>
⃞<ruby>ど⃞⁣⁣う⃞⁣⁣ぶ⃞⁣⁣つ⃞<rp>（</rp><rt>動物</rt><rp）</rp></ruby>み⃞⁣⁣た⃞⁣⁣い⃞⁣⁣で⃞⁣⁣
⃞⁣⁣ま⃞⁣⁣だ⃞<ruby>う⃞⁣⁣ご⃞<rp>（</rp><rt>動</rt><rp）</rp></ruby>け⃞⁣⁣な⃞⁣⁣い⃞⁣⁣な⃞⁣⁣
⃞<ruby>ひ⃞⁣⁣よ⃞⁣⁣り⃞⁣⁣み⃞<rp>（</rp><rt>日和見</rt><rp）</rp></ruby>の⃞<ruby>め⃞⁣⁣っ⃞⁣⁣せ⃞⁣⁣ー⃞⁣⁣じ⃞<rp>（</rp><rt>メッセージ</rt><rp）</rp></ruby>
⃞<ruby>ば⃞<rp>（</rp><rt>化</rt><rp）</rp></ruby>け⃞⁣⁣た⃞<ruby>め⃞⁣⁣い⃞⁣⁣ろ⃞<rp>（</rp><rt>迷路</rt><rp）</rp></ruby>の⃞<ruby>す⃞⁣⁣え⃞<rp>（</rp><rt>末</rt><rp）</rp></ruby>
⃞<ruby>ま⃞⁣⁣っ⃞⁣⁣た⃞⁣⁣ん⃞⁣⁣か⃞⁣⁣か⃞⁣⁣く⃞<rp>（</rp><rt>末端価格</rt><rp）</rp></ruby>の⃞<ruby>あ⃞⁣⁣い⃞⁣⁣ら⃞⁣⁣び⃞⁣⁣ゅ⃞⁣⁣ー⃞<rp>（</rp><rt>アイラビュー</rt><rp）</rp></ruby>
⃞⁣⁣そ⃞⁣⁣の⃞⁣⁣ひ⃞⁣⁣と⃞⁣⁣つ⃞⁣⁣で⃞<ruby>せ⃞⁣⁣か⃞⁣⁣い⃞<rp>（</rp><rt>世界</rt><rp）</rp></ruby>は⃞⁣⁣こ⃞⁣⁣ん⃞⁣⁣な⃞⁣⁣に⃞⁣⁣も⃞⁣⁣
⃞⁣⁣ね⃞⁣⁣ぇ⃞<ruby>ぜ⃞⁣⁣っ⃞⁣⁣さ⃞⁣⁣ん⃞⁣⁣ど⃞⁣⁣こ⃞<rp>（</rp><rt>絶賛何処</rt><rp）</rp></ruby>ぞ⃞⁣⁣の⃞<ruby>ま⃞⁣⁣り⃞⁣⁣お⃞⁣⁣ね⃞⁣⁣っ⃞⁣⁣と⃞<rp>（</rp><rt>マリオネット</rt><rp）</rp></ruby>
⃞<ruby>き⃞⁣⁣ざ⃞<rp>（</rp><rt>刻</rt><rp）</rp></ruby>ま⃞⁣⁣れ⃞⁣⁣た⃞⁣⁣「⃞<ruby>い⃞<rp>（</rp><rt>良</rt><rp）</rp></ruby>い⃞<ruby>こ⃞<rp>（</rp><rt>子</rt><rp）</rp></ruby>」⃞⁣⁣の⃞⁣⁣A⃞⁣⁣ ⃞⁣⁣t⃞⁣⁣o⃞⁣⁣ ⃞⁣⁣Z⃞⁣⁣
⃞⁣⁣あ⃞⁣⁣た⃞⁣⁣し⃞<ruby>せ⃞⁣⁣い⃞⁣⁣じ⃞⁣⁣ん⃞⁣⁣く⃞⁣⁣ん⃞⁣⁣し⃞<rp>（</rp><rt>聖人君子</rt><rp）</rp></ruby>で⃞⁣⁣あ⃞⁣⁣り⃞⁣⁣た⃞⁣⁣い⃞⁣⁣の⃞⁣⁣
⃞<ruby>ち⃞⁣⁣ゅ⃞⁣⁣う⃞⁣⁣し⃞⁣⁣ょ⃞⁣⁣う⃞<rp>（</rp><rt>中傷</rt><rp）</rp></ruby>も⃞<ruby>ひ⃞⁣⁣ぼ⃞⁣⁣う⃞<rp>（</rp><rt>誹謗</rt><rp）</rp></ruby>も⃞<ruby>ま⃞<rp>（</rp><rt>真</rt><rp）</rp></ruby>っ⃞<ruby>ぴ⃞⁣⁣ら⃞<rp>（</rp><rt>平</rt><rp）</rp></ruby>で⃞⁣⁣さ⃞⁣⁣
⃞<ruby>せ⃞⁣⁣い⃞⁣⁣ひ⃞⁣⁣ん⃞⁣⁣か⃞⁣⁣ち⃞<rp>（</rp><rt>製品価値</rt><rp）</rp></ruby>だ⃞⁣⁣け⃞<ruby>ち⃞⁣⁣ょ⃞⁣⁣う⃞⁣⁣だ⃞⁣⁣い⃞<rp>（</rp><rt>頂戴</rt><rp）</rp></ruby>な⃞⁣⁣
⃞<ruby>え⃞⁣⁣が⃞⁣⁣お⃞<rp>（</rp><rt>笑顔</rt><rp）</rp></ruby>は⃞<ruby>と⃞<rp>（</rp><rt>解</rt><rp）</rp></ruby>け⃞⁣⁣な⃞⁣⁣い⃞⁣⁣
⃞⁣⁣ま⃞⁣⁣だ⃞<ruby>う⃞⁣⁣ご⃞<rp>（</rp><rt>動</rt><rp）</rp></ruby>け⃞⁣⁣な⃞⁣⁣い⃞⁣⁣ま⃞⁣⁣ん⃞⁣⁣ま⃞⁣⁣
⃞<ruby>ふ⃞⁣⁣ら⃞<rp>（</rp><rt>フラ</rt><rp）</rp></ruby>つ⃞⁣⁣い⃞⁣⁣た⃞<ruby>す⃞⁣⁣て⃞⁣⁣っ⃞⁣⁣ぷ⃞<rp>（</rp><rt>ステップ</rt><rp）</rp></ruby>
⃞<ruby>ふ⃞<rp>（</rp><rt>踏</rt><rp）</rp></ruby>み⃞<ruby>は⃞⁣⁣ず⃞<rp>（</rp><rt>外</rt><rp）</rp></ruby>さ⃞⁣⁣な⃞⁣⁣い⃞⁣⁣よ⃞⁣⁣う⃞⁣⁣に⃞⁣⁣
⃞⁣⁣ほ⃞⁣⁣ら⃞<ruby>ぜ⃞⁣⁣ん⃞⁣⁣ぶ⃞⁣⁣ぜ⃞⁣⁣ん⃞⁣⁣ぶ⃞<rp>（</rp><rt>全部全部</rt><rp）</rp></ruby>が⃞⁣⁣
⃞<ruby>さ⃞⁣⁣い⃞⁣⁣て⃞⁣⁣き⃞<rp>（</rp><rt>最適</rt><rp）</rp></ruby>で⃞⁣⁣あ⃞⁣⁣る⃞⁣⁣よ⃞⁣⁣う⃞⁣⁣に⃞
```

아 이번엔 배포하기 귀찮은 이유가 있어. 디버깅 귀찮아. 난 못해.