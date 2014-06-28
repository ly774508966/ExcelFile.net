ExcelFile.net
=============

A Excel File Writer based on NPOI.

    var excel = new ExcelFile();
    excel.Sheet("test sheet");
    excel.Row().Cell("test1").Cell(2);
    excel.Row().Cell("test2").Cell(3);
    excel.Save("a.xls");

![](/images/a.JPG)

	var excel2 = new ExcelFile();
    excel2.Sheet("test2 sheet");
    excel2.Row(25, excel2.NewStyle().Background(HSSFColor.Yellow.Index)).Empty(2).Cell("test1");
    excel2.Row(15).Empty().Cell(1).Cell(2, excel2.NewStyle().Color(HSSFColor.Red.Index));
    excel2.Save("b.xls");

![](/images/b.JPG)

## reference
### ExcelFile
���ݣ�������Sheet()����Row()����Ԫ��Cell()���յĵ�Ԫ��Empty()���ϲ���Ԫ��Cell()
��Ԫ����ʽ��Ĭ����ʽStyle������ʽNewStyle()��������ʽCell()������ʽRow()
����ʽ���п�Sheet()
����ʽ��Ĭ���и�DefaultRowHeight()�������и�Row()
����������ļ�Save()��Զ������Save()

### ExcelStyle
����ɫ��Background
�߿򼰱߿���ɫ��Border��BorderTop��BorderBottom��BorderLeft��BorderRight
���룺Align��VerticalAlign
���֣�WrapText��Italic��Underline��FontSize��Font��Color��Bold

## nuget
You can get [it](https://www.nuget.org/packages/ExcelFile.net) from Nuget.