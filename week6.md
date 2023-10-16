## Week 6 - Tim Honiset 40595819

Given the issues surrounding the lab materials for week 7, this week's porfolio will focus just on the unit test that I written, tested, uploading into repo and merging into the main brach

# The Unit Test

Below is the xUnit test based on the TestSelectedWord() method.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

using Hangman;
using NuGet.Frameworks;

namespace UnitTestProject
{
   
    public class TestSelectedWord
    {

        [Fact]
        public void Test_Easy_Test_Selected_Word()
        {
            List<string> Words = new List<string> { "apple", "car", "float" };

            GamePage gp = new GamePage();

            string word = gp.SelectWord("Easy");

            Assert.Contains(word, Words);   
            
        }

        [Fact]
        public void Test_Medium_Test_Selected_Word()
        {
            List<string> Words = new List<string> { "bananas", "flopper", "streaker" };

            GamePage gp = new GamePage();

            string word = gp.SelectWord("Medium");

            Assert.Contains(word, Words);

        }

        [Fact]
        public void Test_Hard_Test_Selected_Word()
        {
            List<string> Words = new List<string> { "establishment", "frictionless", "distinguish" };

            GamePage gp = new GamePage();

            string word = gp.SelectWord("Hard");

            Assert.Contains(word, Words);

        }

    }
}


The unit test was initiated by highlighting the test method, right clicking and selecting run test (fig 1)

![](/images/vs-run-unit-tets.png "")

**fig 1**

The unit test passed as shown in figure 2

![](/images/vs-tets-passed.png "")

**fig2**

Once the tests were successfull, my feature test branch was pushed into GitHub (fig 3)

![](/images/github-push-branch.png "")

**fig 3**

Using GitHub, my test branch was merged into the main branch

![](/images/github-merged-branch.png "")

**fig 4**
