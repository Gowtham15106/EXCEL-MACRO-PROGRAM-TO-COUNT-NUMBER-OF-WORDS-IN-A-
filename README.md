# EXCEL-MACRO-PROGRAM-TO-COUNT-NUMBER-OF-WORDS-IN-A-SOURCE CODE:Sub CountWordsInSelectedRange()Dim rng As Range, cell As RangeDim cellWords As Integer, totalWords As IntegerDim content As String' Set the selected rangeSet rng = SelectiontotalWords = 0' Loop through each cell in the rangeFor Each cell In rngIf Not cell.HasFormula Thencontent = Trim(cell.Value)If content = "" ThencellWords = 0ElsecellWords = 1' Count spaces to determine number of wordsDo While InStr(content, " ") > 0content = Mid(content, InStr(content, " ") + 1)content = Trim(content)cellWords = cellWords + 1Loop
