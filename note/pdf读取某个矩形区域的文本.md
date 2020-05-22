## 需求

解析pdf某个区域内的数据

## jar包依赖

pdfbox-2.0.19.jar

fontbox-2.0.19.jar

commons-logging-1.2.jar

**maven**

```xml
<!-- https://mvnrepository.com/artifact/org.apache.pdfbox/pdfbox -->
    <dependency>
        <groupId>org.apache.pdfbox</groupId>
        <artifactId>pdfbox</artifactId>
        <version>2.0.19</version>
    </dependency>
```

## 基础代码

```
String pathname = "";//文件路径
int x = 0;
int y = 0;
int width = 100;
int height = 100;

File file = new file(pathname);
PDDocument doc = PDdocument.load(file);
PDPage page = doc.getPages().get(0);
Rectangle2D rect  = new Rectangle(x, y, width, height);

PDFTextStripperByArea stripper = new PDFTextStripperByArea();
stripper.setSortByPosition(true);
stripper.addRegion("regionName", rect);
stripper.extractRegions(page);
String text = stripper.getTextForRegion("regionName");
```

原点在右上角，向左为x正，向下为y正

## 获取区域坐标

将pdf转化为图片 用画图工具打开

```
String pathname = "";
File file = new File(pathname);
String fileName = file.getName();
fileName = fileName.substring(0, fileName.lastIndexOf("."));
PDDocument doc = PDdocument.load(file);

PDFRenderer render = new PDFRenderer(doc);
BufferedImage bufferedImage = render.renderImage(0);
ImageIO.write(bufferedImage, "png", new File(fileName + ".jpg"));
```



## 简单封装

```
public class PdfUtil(String pathname){
  /**
     * pdf转化为图片
     * 
     * @param pathname
     *            文件路径
     * @param formatName
     *            文件类型 png img gif
     * @throws IOException
     */
    public static void toImage(String pathname, String formatName) throws IOException {
        File file = new File(pathname);
        PDDocument document = PDDocument.load(file);
        String parent = file.getParent();
        String fileName = file.getName();
        int lastIndexOf = fileName.lastIndexOf(".");
        fileName = fileName.substring(0, lastIndexOf);
        PDFRenderer render = new PDFRenderer(document);
        for (int i = 0, size = document.getNumberOfPages(); i < size; i++) {
            BufferedImage bufferedImage = render.renderImage(i);
            ImageIO.write(bufferedImage, formatName, new File(parent, fileName + "_" + i + "." + formatName));
        }
    }
    
    /**
     * 读取pdf区域文本
     * @param pathname
     * @param x
     * @param y
     * @param width
     * @param height
     * @return
     * @throws IOException
     */
    public static String readByArea(String pathname, int x, int y, int width, int height) throws IOException {
        PDDocument load = PDDocument.load(new File(pathname));
        PDPage page = load.getPages().get(0); //第一页
        Rectangle2D rect = new Rectangle(x, y, width, height);
        PDFTextStripperByArea stripper = new PDFTextStripperByArea();
        stripper.setSortByPosition(true);
        stripper.addRegion("regionName", rect);
        stripper.extractRegions(page);
        return stripper.getTextForRegion("regionName");
    };
}
```



## 延伸

