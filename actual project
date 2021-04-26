import random
print ('Let\'s play Rock Paper Scissors!')
tokenbank=5
tokenbet=0
rock=1
paper=2
scissors=3
userrock=('rock')
userpaper=('paper')
userscissors=('scissors')
computermove=4
usermovechoice=4
playagain=('n')
def actualgame():
  global computermove
  computermove=random.randint(1, 3)
  global tokenbet
  tokenbet=input(f'How many tokens would you like to bet? You currently have {tokenbank} tokens. You can bet up to 2 tokens only if you have at least 2. ')
  invalid_tokenbet()
def movechoice():
  global usermovechoice
  usermovechoice=input('Choose rock, scissors or paper. ')
  RockPaperScissors()
def RockPaperScissors():
  global usermovechoice
  if usermovechoice==userrock:
    if computermove==scissors:
      print('The computer chose scissors')
      win()
    elif computermove==paper:
      print ('the computer chose paper')
      loss()
    elif computermove==rock:
      print ('the computer chose rock')
      tie()
  elif usermovechoice==userpaper:
      if computermove==rock:
        print ('The computer chose rock')
        win()
      elif computermove==paper:
        print ('the computer chose paper')
        tie()
      elif computermove==scissors:
        print ('the compuer chose scissors')
        loss()
  elif usermovechoice==userscissors:
    if computermove==paper:
      print ('the computer chose paper')
      win()
    elif computermove==rock:
      print ('the computer chose rock')
      loss()
    elif computermove==scissors:
      print ('the computer chose scissors')
      tie()
  else:
    print ('all lower case please with correct spelling of rock paper or scissors with no spaces')
    movechoice()
def win():
  global tokenbank
  tokenbank=tokenbet+tokenbank
  global playagain
  playagain=input(f'Congradulations you have won. Would you like to play again? Enter y for yes or n for no. ')
  invalid_playagain()
def loss():
  global tokenbank
  tokenbank=tokenbank-tokenbet
  global playagain
  if tokenbank>0:
    playagain=input('I am sorry you have lost. Would you like to play again? Enter y for yes or n for no. ')
    invalid_playagain()
  elif tokenbank<=0:
    print ('Game Over')
def tie():
  global playagain
  playagain=input (f'Congradulations you have tied. Would you like to play again? Enter y for yes or n for no. ')
  invalid_playagain()
def invalid_tokenbet():
  global tokenbet
  if tokenbet==('1'):
    tokenbet=1
    movechoice()
  elif tokenbet==('2'):
    tokenbet=2
    if tokenbet>tokenbank:
      tokenbet=input('you only have 1 token to bet. please choose to bet 1 token ')
      invalid_tokenbet()
    else:
      movechoice()
  elif tokenbet!=('1') or tokenbet!=('2'):
    tokenbet=input('please choose the number 1 or 2 ')
    invalid_tokenbet()
def invalid_playagain():
  global playagain
  if playagain==('y'):
    actualgame()
  elif playagain==('n'):
    print ('Thank you for playing!')
  else:
    playagain=input('please choose y or n ')
    invalid_playagain()
actualgame()
