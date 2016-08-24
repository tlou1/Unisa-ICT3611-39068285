# Unisa-ICT3611-39068285
GGG Athletic Club

    Private Sub btnClose_Click(sender As Object, e As EventArgs) Handles btnClose.Click
        Close()
    End Sub

    

    Private Sub btnRecord_Click(sender As Object, e As EventArgs) Handles btnRecord.Click
        'input Data in textbox and list box
        Me.txtName.Text = ""
        Me.txtSurname.Text = ""


        'check radiobutton for male and female

        Dim Gender As String
        If Radiofemale.Checked Then
            Gender = "female"
        ElseIf Radiomale.Checked Then
            Gender = "male"
        End If



    End Sub

    Private Sub Members_SelectedIndexChanged(sender As Object, e As EventArgs) Handles Members.SelectedIndexChanged

        ' Get the currently selected item in the ListBox.
        Dim curItem As String = Members.SelectedItem.ToString()

        ' Find the string in members list box.
        Dim index As Integer = Members.FindString(curItem)
        ' If the item was not found in ListBox 2 display a message box, otherwise select it in ListBox2.
        If index = -1 Then
            MessageBox.Show("Item is not available in ListBox2")
        Else
            Members.SetSelected(index, True)
        End If
    End Sub

End Class
