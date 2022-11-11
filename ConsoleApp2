using System;
using System.Collections.Generic;
using static System.Random;
using System.Text;

namespace ConsoleApp2
{
    internal class Program
    {
        private static void printHangman(int wrong) {
            if (wrong == 0)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("         |");
                Console.WriteLine("         |");
                Console.WriteLine("         |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 1) {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine("         |");
                Console.WriteLine("         |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 2)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine("  |      |");
                Console.WriteLine("         |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 3)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine(" /|      |");
                Console.WriteLine("         |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 4)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine(" /|\\    |");
                Console.WriteLine("         |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 5)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine(" /|\\    |");
                Console.WriteLine(" /       |");
                Console.WriteLine("        ===");
            }
            else if (wrong == 6)
            {
                Console.WriteLine("\n+------+");
                Console.WriteLine("  O      |");
                Console.WriteLine(" /|\\    |");
                Console.WriteLine(" / \\    |");
                Console.WriteLine("        ===");
            }
        }

        private static int printWord(List<char>guessedLetters, string randomWord) { 
            int counter = 0;
            int rightLetters = 0;
            Console.WriteLine("\r\n");
            foreach (char c in randomWord) {
                if (guessedLetters.Contains(c))
                {
                    Console.Write(c + " ");
                    rightLetters++;
                }
                else {
                    Console.Write(" ");
                }
                counter++;
            }

            return rightLetters;
        }

        public static void printLines(String randomWord) {
            Console.Write("\r");
            foreach (char c in randomWord) {
                Console.OutputEncoding = System.Text.Encoding.Unicode;
                Console.Write("\u0305 ");
            }
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome!");
            Console.WriteLine("______________________________________");

            Random random = new Random();

            List<String> wordDictionary = new List<String> { "extend", "jelly", "sleeve", "guard", "disorder", "sunflower", "house", "diamond", "memes", "yeet", "hello", "howdy", "like", "subscribe" };
            int index = random.Next(wordDictionary.Count);
            String randomWord = wordDictionary[index];
            foreach (char c in randomWord) {
                Console.Write("_ ");
            }

            int length_word = randomWord.Length;
            int wrong = 0;
            List<char> currentLetters_guessed = new List<char>();
            int correct = 0;

            while (wrong != 6 && correct != length_word)
            {
                Console.Write("\nLetters guessed so far: ");
                foreach (char letter in currentLetters_guessed) {
                    Console.Write(letter + " ");
                }
                // prompt
                Console.Write("\nGuess a letter: ");
                char Letters_guessed = Console.ReadLine()[0];
                // checked if letter is already guessed
                if (currentLetters_guessed.Contains(Letters_guessed))
                {
                    Console.Write("\nYou have already guessed this letter");
                    printHangman(wrong);
                    correct = printWord(currentLetters_guessed, randomWord);
                    printLines(randomWord);
                }
                else
                {
                    //check if letter is in word
                    bool right = false;
                    for (int i = 0; i < randomWord.Length; i++)
                    {
                        if (Letters_guessed == randomWord[i])
                        {
                            right = true;
                        }
                    }
                    if (right)
                    {
                        printHangman(wrong);
                        currentLetters_guessed.Add(Letters_guessed);
                        correct = printWord(currentLetters_guessed, randomWord);
                        Console.Write("\r\n");
                        printLines(randomWord);
                    }
                    else
                    {
                        wrong++;
                        currentLetters_guessed.Add(Letters_guessed);
                        printHangman(wrong);
                        correct = printWord(currentLetters_guessed, randomWord);
                        Console.Write("\r\n");
                        printLines(randomWord);
                    }
                }
            }
            Console.WriteLine("\r\nGame Over");
        }
    }
}
