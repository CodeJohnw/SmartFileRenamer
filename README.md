# 智能文件命名助手SmartFileRenamer
本项目旨在通过自动化工具实现文件名的管理与优化，流程包括从文件夹读取文件名并生成Excel文件，通过AI对文件名进行分析和优化，用户审核后自动更新文件夹中的文件名。该工具适用于需要批量管理文件的场景，如整理图片、文档或视频等。

---

## 功能介绍  

1. **文件读取与Excel生成**  
   - 从指定文件夹读取所有文件名。  
   - 生成一个包含文件名及超链接的Excel文件，用户可通过超链接快速访问文件。

2. **AI自动命名建议**  
   - 自动分析文件名，提供优化的命名建议（如更符合规范、便于分类）。  
   - 优化建议会写入Excel供用户参考与修改。

3. **用户确认修改并更新文件名**  
   - 用户可直接在Excel中审核和完善AI生成的建议文件名。  
   - 工具读取修改后的Excel文件，自动将文件夹中的文件名更新为新文件名。

4. **可选扩展功能**  
   - 日志记录：记录文件名修改的历史，便于回溯。  
   - 文件备份：保存原始文件名列表，确保可随时回滚。  
   - 类型过滤：仅处理特定文件类型（如图片、视频、文本）。  

---

## 安装与使用

### 环境依赖  
- Python 3.x  
- 依赖库：  
  ```bash
  pip install openpyxl tk
  ```

### 使用步骤  

1. **运行文件读取与Excel生成模块**  
   - 运行脚本，选择需要整理的文件夹。  
   - 程序会在目标文件夹中生成一个包含文件名及超链接的Excel文件。  

2. **AI生成命名建议**  
   - 运行AI模块，读取Excel文件的文件名，自动生成优化的命名建议。  
   - 程序会将建议的文件名写入Excel的指定列。

3. **用户确认并更新文件名**  
   - 在Excel中审核并修改AI建议的文件名。  
   - 运行更新模块，程序会读取Excel并更新目标文件夹中的文件名。

---

## 项目结构  

```
project_folder/
│
├── main.py                 # 主程序入口
├── read_files_to_excel.py  # 生成Excel文件的模块
├── ai_rename.py            # AI自动生成命名建议的模块
├── update_filenames.py     # 根据Excel更新文件名的模块
├── requirements.txt        # 项目依赖
└── README.md               # 项目说明
```

---

## 注意事项  
1. 请确保文件夹中的文件名不含特殊字符，以免引发路径问题。  
2. 确认Excel中所有新文件名的唯一性，避免重名导致覆盖问题。  
3. 建议在操作前备份原始文件，以免误操作导致文件丢失。

---

## 后续改进  

- 增加多语言支持。  
- 支持更多文件管理功能，如自动分类、标签化命名等。  
- 提供可视化界面，简化用户操作。

--- 

## 许可证  
该项目使用 MIT License 进行许可。
