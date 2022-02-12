using Microsoft.VisualStudio.TestTools.UnitTesting;
using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;
using OpenQA.Selenium.Firefox;
using System;
using System.Threading;

namespace Automation_assignment_01
{
    [TestClass]
    public class XpathAttribute
    {
        
        public void Login()
        { 
       
        
        }


        [TestMethod]
        //using @text()
        public void XpathLocatorTextFunctions()
        {
           // IWebDriver driver= new FirefoxDriver();
          IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            string s1 = driver.FindElement(By.XPath(".//h2[text()='Our People']")).Text;
            Console.WriteLine(s1);
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @contain()
        public void XpathLocatorContainFunctions()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            string s2 = driver.FindElement(By.XPath(".//input[contains(@d,'Me')]")).Text;
            Console.WriteLine(s2);
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]

        //using @Not()
        public void XpathLocatorNotFunctions()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath(".//input[@type='checkbox' and  not(@checked)]"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @last()
        public void XpathLocatorlastFunctions()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath(".//tbody/tr[last()]"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @position()
        public void XpathLocatorpositionFunctions()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("(.//input[@type='text'])[position()=2]"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @Parent filter
        //
        public void XpathLocatorParentFilter()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//h1/parent::div"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @Child filter
        //
        public void XpathLocatorChildFilter()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//footer/child::p"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @followingsibling
        //
        public void XpathLocatorfollowingsibling()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//tr[6]/following-sibling::tr"));
            Thread.Sleep(2000);
            driver.Quit();
        }
        [TestMethod]
        //using @following
        //
        public void XpathLocatorfollowing()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//tr[6]/following::*"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @preceding-sibling:
        //
        public void XpathLocatorprecedingsibling()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//tr[6]/preceding-sibling::tr"));
            Thread.Sleep(2000);
            driver.Quit();
        }
        [TestMethod]
        //using @ancestor:
        //
        public void XpathLocatorancestor()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//table/ancestor::div"));
            Thread.Sleep(2000);
            driver.Quit();
        }

        [TestMethod]
        //using @descendant:
        //
        public void XpathLocatordescendant()
        {
            // IWebDriver driver= new FirefoxDriver();
            IWebDriver driver = new ChromeDriver();
            driver.Url = "http://ankpro.com/";
            driver.FindElement(By.XPath("//table/descendant::td"));
            Thread.Sleep(2000);
            driver.Quit();
        }
    }
}

