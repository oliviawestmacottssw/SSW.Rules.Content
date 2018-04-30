---
type: rule
archivedreason: 
title: Do you always create suggestions when something is hard to do?
guid: 7058fd5e-0a18-4f25-b085-c499a2c5ab17
uri: do-you-always-create-suggestions-when-something-is-hard-to-do
created: 2018-04-30T22:04:43.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>One of our goals is to make the job of the developer as easy as possible. If you have to write a lot of code for something that you think you should not have to do, you should make a suggestion and add it to the relevant page.</p><p>If you have to add a suggestion, make sure that you put the link to that suggestion into the comments of your code.​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​Imports System.Windows.Threading<br>Imports System.Threading<br>''' &lt;summary&gt;<br>''' base class for command implementations <br>''' This is a work around as standard MVVM commands <br>''' are not provided by default<br>''' &lt;/summary&gt;<br>''' &lt;remarks&gt;&lt;/remarks&gt;<br>Public MustInherit Class Command<br> Implements ICommand<br> Private m_dispatcher As Dispatcher<br> Protected Sub New()<br> If Not Application.Current Is Nothing Then<br> m_dispatcher = Application.Current.Dispatcher<br> Else<br> m_dispatcher = Dispatcher.CurrentDispatcher<br> End If<br> Debug.Assert(Not m_dispatcher Is Nothing)<br> End Sub<br> Public MustOverride Function CanExecute(ByVal parameter As Object) As Boolean Implements System.Windows.Input.ICommand.CanExecute<br> Public MustOverride Sub Execute(ByVal parameter As Object) Implements System.Windows.Input.ICommand.Execute<br> Public Event CanExecuteChanged(ByVal sender As Object, ByVal e As System.EventArgs) Implements System.Windows.Input.ICommand.CanExecuteChanged<br><br> Public Sub OnCanExecuteChanged()<br> If Not m_dispatcher.CheckAccess Then<br> m_dispatcher.Invoke(New ThreadStart(AddressOf OnCanExecuteChanged), DispatcherPriority.Normal)<br> Else<br> CommandManager.InvalidateRequerySuggested()<br> RaiseEvent CanExecuteChanged(Me, New EventArgs)<br> End If<br> End Sub<br>End Class</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example - The link to the suggestion should be in the comments​<br></dd><p class="ssw15-rteElement-CodeArea">​Imports System.Windows.Threading<br>Imports System.Threading<br>''' &lt;summary&gt;<br>''' base class for command implementations <br>''' This is a work around as standard MVVM commands <br>''' are not provided by default<br>''' http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/WPF.aspx#EmbraseMVVM<br>''' &lt;/summary&gt;<br>''' &lt;remarks&gt;&lt;/remarks&gt;<br>Public MustInherit Class Command<br> Implements ICommand<br> Private m_dispatcher As Dispatcher<br> Protected Sub New()<br> If Not Application.Current Is Nothing Then<br> m_dispatcher = Application.Current.Dispatcher<br> Else<br> m_dispatcher = Dispatcher.CurrentDispatcher<br> End If<br> Debug.Assert(Not m_dispatcher Is Nothing)<br> End Sub<br> Public MustOverride Function CanExecute(ByVal parameter As Object) As Boolean Implements System.Windows.Input.ICommand.CanExecute<br> Public MustOverride Sub Execute(ByVal parameter As Object) Implements System.Windows.Input.ICommand.Execute<br> Public Event CanExecuteChanged(ByVal sender As Object, ByVal e As System.EventArgs) Implements System.Windows.Input.ICommand.CanExecuteChanged<br><br> Public Sub OnCanExecuteChanged()<br> If Not m_dispatcher.CheckAccess Then<br> m_dispatcher.Invoke(New ThreadStart(AddressOf OnCanExecuteChanged), DispatcherPriority.Normal)<br> Else<br> CommandManager.InvalidateRequerySuggested()<br> RaiseEvent CanExecuteChanged(Me, New EventArgs)<br> End If<br> End Sub<br>End Class</p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; Good example - Wh​​en you link to a suggestion everyone can find it and vote it up</dd><p>​<br></p>


