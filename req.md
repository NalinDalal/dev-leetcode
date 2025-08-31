# Dev contest platform similar to codeforces

Open a landing page you see some of challenges
Challenges have sub challenges listed like contest

Contest page
Based on timer sub-challneges to do with time constraints, ui to attempt them
Show testcases you passed
Points

SubChallenge page
Lhs has challenge listed out,
Rhs has editor

Test cases:
Ai
Submit docker file
Deploy own code
Codecrafter

Push to GitHub, docker build happens

Real time leaderboard:
Redis sorted sets via cache

To ans queries use in memory priority queue

---

Stage 1

0. MonoRepo

1. Add authentication -- login via email + otp
2. Add respective middlewares
3. Admins can create a contest, add sub challenges in there.
4. User can see all the challenges.
5. User can get a challenge if it is already started
6. User can try to submit a challenge

Stage 2

1. Implement the / submit endpoint. Whatever resposne we get back from the AI, store it in the DB, also store it in the redis sorted set
2. Leaderboard - during the contest - get it from the redis sorted set
3. Post contest - Recalculate the leaderboard and store it in the DB

Stage 3

1. Write the frontend
2. Integrate with the backend

submit:
have rate limiting
max 20 per second
