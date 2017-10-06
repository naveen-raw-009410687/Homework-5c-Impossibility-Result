# Homework-5c-Impossibility-Result
Homework 5c - Impossibility Result Given an anonymous ring, prove that it is impossible to elect a leader. 
Solution 1: Lemma After round k of any deterministic algorithm on an anonymous ring, each node is in the 
same state Sk. 
By induction: all nodes start in same state, and each round consists of sending, receiving and performing local computations. All nodes send the same messages, receive the same messages, and do the same computations. So they always stay in same state, So when a node decides to become a leader, then all others do too. 
OR Solution 2 : Prove the impossibility result for leader election for the anonymous ring. Theorem: There is no leader election algorithm for anonymous rings, 
Proof Sketch: 1- Every processor begins in same state with same outgoing messages (since anonymous) 2- Every processor receives same messages, does same state transition, and sends same messages in round 1 3- Ditto for rounds 2, 3, and so on ... 4- Eventually some processor is supposed to enter an elected state. But then they all would. 
OR Solution 3: 
Lemma 3.1: Suppose that for k rounds of algorithm A in a ring R, at the end of round k all processors n have the same message. 
Proof: By induction, base case k = 0. 
For round k-1, the above lemma holds. Since all processors are in the same state at k-1, the same message has been sent to right(m_r) and left(m_l). Then in round k all processors receive previous rounds sent messages m_l and m_r. Thus by round k, all processors receive the same message, without changing their states. Hence a leader cannot be elected, since all processors will enter an elected state. 
