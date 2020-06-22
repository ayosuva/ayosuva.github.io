---
layout: post
title:  "Useful Ranorex Code snippets"
author: Yosuva
categories: [ Ranorex, tutorial ]
image: assets/images/ranorexstudio.jpg
---
This page contains few useful Ranorex code snippets

1. To get current Test case name:
```c#
var curTestCase = (TestCaseNode)TestSuite.CurrentTestContainer;
string tcName = curTestCase.Name;
```
2. To add image in report
```c#
Report.LogData(ReportLevel.Info, "General Data", Ranorex.Imaging.Load(@"E:\Yosuva\Evidence\test.jpg"));
```
3. To get Test status and Test suite status
```c#
var tcStatus = TestSuite.Current.GetTestContainer("tcName").Status; // get status of specified TC 
var tcStatus = Ranorex.Core.Reporting.ActivityStack.Current.Status; // returns test suite status
```
4. To log Html in report
```c#
Report.LogHtml(ReportLevel.Success,"Generated "+filename+" Document", "<a href='"+filename+".pdf"+"' target='_blank'>Open Document</a>");
```
5. Example for Table Iteration:
```c#
public void ValidateReceivedPayments(RepoItemInfo reference_obj, RepoItemInfo cell_amount, RepoItemInfo cell_reason)
        {
            IList<Ranorex.Cell> reference = reference_obj.CreateAdapters<Cell>();
            IList<Ranorex.Cell> ada_amount = cell_amount.CreateAdapters<Cell>(); 
            IList<Ranorex.Cell> ada_reason = cell_reason.CreateAdapters<Cell>();             
            //String mydate=tdate[0].Text;
            //String s1=tDescription[0].Text;
            int listCount =  products.Count;
 
 
            for(int i=0;i<listCount;i++)
            {
                string transaction_ref=reference[i].Text;
                string amount=ada_amount[i].Text;
                string reason=ada_reason[i].Text;
        }
}
```
6. To get the report directory path
```c#
string dest = TestReport.ReportEnvironment.ReportFileDirectory;
```
7. To call module inside module or user code.You can add the below user code into a module.
```c#
public void RunModule()
{
  Recording_module_Name.Start();
}
```
8. Code to get current data range
```c#
string rows = TestSuite.Current.CurrentTestContainer.DataRange.MaxRange.ToString();
```
9. To get custom logo in Ranorex PDF report

   Download the style.xml and specify logo path in the below mentioned line.
   This style.xml can also be used to increase screenshot quality and to change look and feel of pdf.

   ```html
   <global toc="true" logo="C:\logo.png" bottommargin="2" topmargin="2" showtestdata="true" showdescription="true" showpictures="true"/>
   ```
   > Note:In order to see the changes in the pdf , Please specify style.xml path in ConvertToPDF method or in PDF parameters.

10. To parameterize a value in the RxPath or to pass dynamic values in Rxpath.
```c#
//select[#'Category']/option[@value=$Category]
$Category is the parameter/variable name
```
11. To use xpath in user code
```c#
Ranorex.Button Button = Host.Local.FindSingle<Ranorex.Button>("/form[@controlname='RxMainFrame']//tabpage[@controlname='RxTabIntroduction']/button[@accessiblename='Submit']",20000); 
Button.MoveTo();
```
12. To get video path and name
```c#
string folder_path = TestReport.ReportEnvironment.ReportVideoFolderPath;
string folder_name = TestReport.ReportEnvironment.ReportVideoFolderName;  
string file_name = TestReport.ReportEnvironment.CurrentVideoFileName; 
```
