

    Part A
        Write down your honest answers: How have you used AI for coding so far? Fixing mistakes, finding alternative ways and learning coding tips and tricks. Do you ask AI for solutions before trying yourself? No, i need to try first for myself. Can you explain code you've submitted without AI's help? 99% of the time i can. What would happen if AI was suddenly unavailable during an exam or interview? I will try my best to find ways to finish it even if they are sub-optimal.
        Identify your current pattern: Which learner are you now? I am a type B learner.
        Write a brief paragraph: Where are you now, and where do you want to be? I am currently learning how to code, and the language models and i want to be a multitasker that works on many levels.

    Part B

        Write pseudocode for a palindrome check 1. take a string 2. filter it 3. test it against itself in reverse 4. see if its palindrome or not Implement your solution in Python solution in go package main

          package main
	
	import (
		"fmt"
	)
	
	func main() {
		// List of example strings to test
		words := []string{
			"racecar",
			"hello",
			"A man a plan a canal Panama",
			"apostopa",
		}
	
		// Go through each string in the list
		for _, w := range words {
	
			// Build a cleaned version: only A–Z and a–z, all lowercase
			clean := ""
			for i := 0; i < len(w); i++ {
				ch := w[i]
	
				// Check if it's a letter
				if (ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z') {
					// Convert uppercase to lowercase
					if ch >= 'A' && ch <= 'Z' {
						ch = ch + 32
					}
					clean += string(ch)
				}
			}
	
			// Check if the cleaned string is a palindrome
			ok := true
			for i := 0; i < len(clean)/2; i++ {
				if clean[i] != clean[len(clean)-1-i] {
					ok = false
					fmt.Println("The palidrome breaks in position:", i+1)
					break
				}
			}
	
			// Print the result and the cleaned string
			fmt.Println(ok, "|", clean)
		}
	}

        Test with examples: racecar, hello, A man a plan a canal Panama Tests pass. Debug any issues yourself . Add comments explaining your logic The pseudocode are the comments.

        Strategic AI use After you have a working solution, ask AI: What's the time complexity? O(n) What edge cases am I missing? Strings with spaces (fix: bufio reader) Empty string or no letters(fix: write a small extention code that checks the x for that) Alternatives and trade-offs?
            Instead of reversing:Build a cleaned string forward and compare clean := make([]byte, 0, len(s))
            Slightly less logical How does it perform on very long strings? Each iteration creates a new string → temporary allocations → high GC pressure on long strings 10⁴ letters Acceptable 10⁵ letters Noticeable delay, ~seconds 10⁶ letters Likely freezes / GC overhead 10⁷ letters Practically unusable

        What did you learn by struggling first? That there is always room for improvement. How is your understanding different than if you'd just asked for the solution? I improved my understanding of this specific code and now can rewrite it based on ai's additions. Can you now implement similar functions (reverse a string, find duplicates) without AI? Yes. What mental model did you build? I dont understand the question.

    part C Already built.

    part D I will use AI when:

     After I've attempted a problem 

     To understand why my solution works/doesn't

     To explore alternatives after I have a working solution

    I will NOT use AI when:

     I haven't tried the problem myself

     I'm taking an assessment or test

     I need to build fundamentals

    I know I'm using AI fairly when:

     I can explain my code without looking at AI's response

     I could solve the problem without AI

     I feel more confident in my abilities

    Giorgos Emmanouil 19 2026 

    Part E: Real-World Scenario Analysis Interview: "Explain how you'd implement a caching system." If you always relied on AI, can you answer? No you cant answer if you always rely on ai. Production bug at 2 AM: AI is unavailable. Can you debug code you don't fully understand? No but with a lot of help from other online sources i could understand it. New tech with little documentation: If you never learned to read docs and experiment, what happens? You overrely on AI and stay behind on your personal knowledge. Write a paragraph: How does using AI fairly now prepare you for these scenarios? I already answered before.

    Part F: Building Irreplaceable Skills

    Rate yourself 1–5 and write an improvement plan for your lowest area:

     Problem decomposition 4

     Systems thinking 3

     Critical evaluation 3

     Debugging mindset 2

     Conceptual understanding (the "why") 5

    Action plan: 3 specific actions this week to improve it without outsourcing thinking to AI. Code more, Re-solve problems, Learn more languages.

