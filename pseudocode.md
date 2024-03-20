Program init
Registration period start
Function Registration - Date and Time restriction
Dataframe - Voters (added to git.ignore)
Properties
- Name
- Email

Dataframe - Nominees
- candidateName
- Integer of Total nominees = choiceTotal
- votes

Function voting period
- Time and date of voting period

function voterBallot
- #1 choice row
- #2 choice row
- #3 choice row
index = choiceTotal
exceptions - one choice per row

function submitBallot

Function voteCount
- voteTotal
- candidateWinner
- nextRound (voterBallot.row + 1)
- ballotTotal
Function runOff

Users choose favorite Candidates 1 to choiceTotal.
Exception - User can choose not to select more than one candidate

If (all users respond or voting period end){
    voteCount
}

Round 1 of voting - choice #1 of voterBallot counted
If (candidateName.votes > 50% ballotTotal)
    {
        candidateWinner
    } else { 
        nextRound
    }
Round 2 of voting - choice #2 of voterBallot
If (candidateName.votes > 50% ballotTotal)
    {
        candidateWinner
    } else { 
        nextRound
    }
Repeat until candidatWinner
Execeptions - Tie
If candidteName.votes !>= 50% ballotTotal
runOff