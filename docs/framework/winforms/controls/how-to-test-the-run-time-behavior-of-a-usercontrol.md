---
title: "How to: Test the Run-Time Behavior of a UserControl"
ms.date: "03/30/2017"
helpviewer_keywords: 
  - "UserControl class [Windows Forms], testing"
  - "user controls [Windows Forms], testing"
  - "composite controls [Windows Forms], testing"
  - "UserControl Test Container"
  - "UserControl class [Windows Forms], run-time behavior"
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
---
# How to: Test the Run-Time Behavior of a UserControl
When you develop a <xref:System.Windows.Forms.UserControl>, you need to test its run-time behavior. You can create a separate Windows-based application project and place your control on a test form, but this procedure is inconvenient. A faster and easier way is to use the **UserControl Test Container** provided by Visual Studio. This test container starts directly from your Windows control library project.  
  
> [!IMPORTANT]
>  For the test container to load your <xref:System.Windows.Forms.UserControl>, the control must have at least one public constructor.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
> [!NOTE]
>  A Visual C++ control cannot be tested using the **UserControl Test Container**.  
  
### To test the run-time behavior of a UserControl  
  
1.  Create a Windows control library project called **TestContainerExample**. For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).  
  
2.  In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Label> control from the **Toolbox** onto the control's design surface.  
  
3.  Press F5 to build the project and run the **UserControl Test Container**. The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.  
  
4.  Select the <xref:System.Windows.Forms.Control.BackColor%2A> property displayed in the <xref:System.Windows.Forms.PropertyGrid> control to the right of the **Preview** pane. Change its value to `ControlDark`. Observe that the control changes to a darker color. Try changing other property values and observe the effect on your control.  
  
5.  Click the **Dock Fill User Control** check box below the **Preview** pane. Observe that the control is resized to fill the pane. Resize the test container and observe that the control is resized with the pane.  
  
6.  Close the test container.  
  
7.  Add another user control to the **TestContainerExample** project. For details, see [How to: Add Existing Items to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).  
  
8.  In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** onto the control's design surface.  
  
9. Press F5 to build the project and run the test container.  
  
10. Click the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls.  
  
## Testing User Controls from Another Project  
 You can test user controls from other projects in your current project's test container.  
  
#### To test user controls from another project  
  
1.  Create a Windows control library project called **TestContainerExample2**. For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).  
  
2.  In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.RadioButton> control from the **Toolbox** onto the control's design surface.  
  
3.  Press F5 to build the project and run the test container. The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.  
  
4.  Click the **Load** button.  
  
5.  In the **Open** dialog box, navigate to **TestContainerExample**.dll, which you built in the previous procedure. Select **TestContainerExample**.dll and click the **Open** button to load the user controls  
  
6.  Use the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls from the **TestContainerExample** project.  
  
## See also

- <xref:System.Windows.Forms.UserControl>
- [How to: Author Composite Controls](how-to-author-composite-controls.md)
- [Walkthrough: Authoring a Composite Control with Visual Basic](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [Walkthrough: Authoring a Composite Control with Visual C#](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [User Control Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))
