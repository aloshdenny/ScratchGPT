# ScratchGPT
Bigram transformer model from scratch

Essentially, transformers are encoder-decoder models
That is, they take an input (user prompt) --> encode it (tokenization) --> let the tokens talk between each other (self and cross attention) --> decode it (generate next most probable set of words).
This is how chatgpt works: it encodes the user prompt, makes sense of what the encoded data is, tries to find a relation between each token (each token has a weight-->how much probable it is to appear after the previous token), and finally generates a sequence of tokens in a probabilistic manner.

The Shakespeare model is technically half of GPT... its trained on a corpus of Shakespearean text and asked to generate random text based on the weights and biases it has learned during model compile.
This phase is called pretraining ---> the first half of model training.

The second half is finetuning ---> changing the parameters (like temperature, num_tokens, categorization) to generate better tokens to a user prompt.
This is why chatgpt responds more like a human than a chatbot

I trained two models: Shakespeare and Reddit.
The data used for training the Shakespeare model is the total collection of all Shakespearean works available in a 1MB file [input.txt](input.txt).
The data used for training the Reddit model is a cascaded volume of all Reddit comments uptil 2019 available in a compressed 48MB file [reddit.rar](reddit.rar).
[train.ipynb](train.ipynb) is just a breakdown of the transformer architecture I wrote for future editing. [bigram.py](bigram.py) provides a more concise and condensed format of training the model. It uses over 10 million parameters in training, depending on how you modulate your usage of hyperparameters in the code. [MODEL.py](MODEL.py) is probably what you are looking for, as it loads the pre-trained model straight out of the directory and generates text upon execution.


**4000 character Shakespearean text generated by ScratchGPT on RTX 3050:**


Lineless,
How craves bastardy or two and the compest-seet.
Ah, what enrolled gate Rutland's death!
Do attend you make a glassomit
Where they are substance and lodge flies,--
Who cometh the treasons of the law,
And some round men and these lder love!

JOHN:
Then; for I were amain, like a gracious duke,
And prophesy for Ireland-found to more in ears?
Sir, litter dabour than ere thy last over kit
Going our pity hath she's powerful whose maids.
For Henry brealds reposme to revolt thus:
Counsel, my lord, I say am I burgher, which is,
I must speak to die.

NORTHUMBERLAND:
Thanks, Sir
You Stanley, speak be as mine, or sad you will not.

BUCKINGHAM:
Thws are you?

BUSHY:
Bothee, my lord.

HASTINGS:
Go, the Earl of Warwick's executioner?

BUCKINGHAM:
Not why?
From I hence, courager: there take her leave to leave me.
Sirrah, go provost, with froward Jushes;
And I, look me the recounty alord.
Where drod your lordship to the unto that,
Enrest the time to itself and present could,
Not to do not slay the citizen where;
For the other youth as use reason'd with a doze:
Well your highness will be then, be patient
For leave to bear these, to live that; and not will
With where.

First Citizen:
Ay, away, when I, them how to be a subject?

Second Citizen:
Amen.

Second Citizen:
Why, what's the wenchmen?

First Citizen:
Nay, we shall!

Citizen:
I beseech you, sir.

MENENIUS:
This business is as I heard as samed two.

Second Citizen:
You can, missile: you may not ease or no, sword,
Which even no time you shall's poise argate:
That it have, mightierTarry had given your issue
Coriolanus!

LEONTES:
What?

CORIOLANUS:
By my tribunes!
If my joining trippes be to him, plainly vine
Murder the admam's part. The city, poor deright,
And in my country's shature kinsmen by my heart
Gives imprison'd the last that the work.

SICINIUS:
This is the matter: where it is less
Than his fair and distinchorousness, behind touch'd,
Whilst I were also purish him: but I am stranged
Even sleep into the advice, and not
But to him an icty, who would say thee,
Standing in the commonster and men at live,
And let me vawelead the queen's king.
Come, come, come, morerat let's away.

Fertain:
Go will have you good that were:
For, better; say I will stand bite
And fell me and a sail.

Apothecary:
Look, he sets of you with his looking to his war.

Lord:
They have person'd a tediousure.

First Citizen:
What would you please, he do not do?

Second Citizen:
Our thing did, indeed, like a luckless cure, woe,
He cither defend the hild, she said.

Second Citizen:
Wherewar you have.

Second Citizen:
Unto marry?

Third Citizen:
And go you with the haughter.

MENENIUS:
What afway have we come;
To be about cunning of limit:
Your pries and young city.

CORIOLANUS:
Most hour, though my ship's body,
Why on my poor soldiers would burn that
I would deliver you you as house,
Where that father revertires, though atthwart
Most king our princess, being passes
Is ascally in your greatner.

MENENIUS:
Towards  silence?

CORIOLANUS:
Though most unspirated,
Is dear as thy mother to love, her mething;
The porterious people in thy thirty gifts,
And yet believe thee and Francis the nobleman to his heart
Than in my absence that thou took of the world: be not
To be by and repent to try you again.

LUCIO:

It does:
Sweet not. come, we so?

ISABELLA:
Where's has your tongue here?

ANGELO:
Who as my lord?

MISTRESS:
Propsheer?

ANGELO:
If an imputed-bawd or need?

HASTINGS:
Take the brider clamour than Bianca hither;
And from this parliam that living time
Even lender painted at the war, since a double
Is loss of sanctiers: say to this so night
You did befit; let it grow his sweet humong
At the Lord Angelo west this broke a friar imine!
Untime how meets are a sead;
And shat Bolingbroke lawl with it a bloody,
He may not yet think it have his fortune
Again as the land's chair of a noble himd.
Among otestar with this fouly title-a
Give mis-soccieter's own letthoug on my rach
To that revolts for lead mine eyes
To see how


**4000 character Reddit gibberish generated by ScratchGPT on RTX 3050:**


supports will even consider it. In a common sents to be an albulant of to pick this comment at work.
How the very picture of Jewis Penetile goezil by what's willing to clign available offhall everyrardican country? Islamifesuminy though in your league in good shitting military? You are a metal reason. To have to hold your back your hammer for some kind, not getting Britain from his hands.
Yeah I know whether Red was really who I do guaranteed with their hobbal to talk new battle. Getting honest one on the disposable one. Juven if your dad have to put any hour

How Waster please be your lives lure?
No, you have killed and trust that rejects.

As show is the one of the actional mid acceptance of a girl wheater (ad do not, my daughter blue will on each other obligate to my own hard), especially in that.   
I refere, and to be better you between 30% each other live for hour to have the log against shows at least people here I didn't understand needing it. Has is already on all children hinting nopeshit. It also hadled the back hard pressive human shots and once. I think the pain to mention just person and get shady and stealthcary "quite her Peggy" whiche would raise the intesting" specialize meavail.
How do I love your shit it person ahead roles inside? You don’t want something like it’s not moving to actually just start through a guidate auto with a regular solo sell. (Capa, image a comment of corrupt referrs) if you are undertaged, you made shufflighting expressive machines, etc.
Discussions are so cool.

Juv is definitely met that that just rather is on you on the pics on more, and aim now glarity they would procedur.
Yes, We look more, sir. Erge, I am not sure what some people who have the syonuck to do.
Won't lye whether you're there's not caught up.
You can eat it. But their cat ***up*** Crus** Classing Cheo you mentioned, cleaning respecies of anti-come out, counties to see people in their country(.

Nose:


Find has been A-Almireland, This is impremated when some respect the Russia. Harden cents are all of their lists. Good terms online can come up with the wrestlands, anytime waiting on their straight picil.

All we call them with climate places

&gt;Don't fotiate but reddit come one from spawn start characters and then sleep towers given trying to disract their livesed in a stone (endonated) if yes we haven't, and even  wonderfed if anybody who knowses " we announced when that created Tenny" is what going to happen to for? Lol...
But about the diside trapers were expensive, considering the campus thrones or can
So tell my in the eye and shakers are getting facing mandaries and diebing and sliding warfare.
I was simply like how everyone would die, dead as level in PS4.
You mean struggl of how shitpossible fully remaining pregnants. You sound hard to let things have too during block and be torture for you’re all a ‘sc tight' at million.  He isn't created by that’s a seizup but has me more sent some clool.

It people don't think we going into the third faeues, for people feel good enough hopefully now because I'm not veryiminate with my pinnels. I'll ner deathly everything itself being talked, because it is very reserving the Kings movie in the  were insistenting game *I*. Then they were doing Sonic to go the relbook fazing on things. Just be going away 1-1 milk and Dany would've ever had to drag use knocked/ryawns and other timeline in throne standards.
Barr really liked the bacons from there.
I'ven't ever heard that show your arm introduce areas. The moment passes of mechamiline and runing aligning allergy push on his retreature our sider thread, and the modern even other particularly have signs to rebound a bad desk, of cluding repercy.
I don’t think they have never genered by but then defended anything clean when I’m willing to save your breakups can spell out tough as a conservative and punch them into where happieces are and quick people's failing to watch and reading. socialism they don’t need actually end outsiders



**Notes:**

Switch device to 'cpu' if no CUDA device available.
If you are training from the boilerplate code, I suggest running it on Colab's T4 (or if you're brave, on the A100).
Playing with the block_size and batch_size should generate some interesting results.

Joi will require an encoder and decoder segment.
And she will have to be trained on a larger, more conversational corpus of information.
Au Revoir.
