# Liquirizia.FileSystemObject.Implements.FileSystem
FileSystemObject Implementation of Liquirizia for FileSystem

## Sample
```python
from Liquirizia.FileSystemObject import FileSystemObjectHelper
from Liquirizia.FileSystemObject.Implements.FileSystem import FileSystemObject, FileSystemObjectConfiguration

if __name__ == '__main__':

	# 파일시스템 사용 설정	
	FileSystemObjectHelper.Set(
		'Sample',
		FileSystemObject,
		FileSystemObjectConfiguration('.')
	)

	# 파일 시스템 가져오기
	fo = FileSystemObjectHelper.Get('Sample')

	# 파일 생성 및 쓰기
	with fo.open('Sample.txt', 'w') as f:
		f.write('Hello World')
		f.close()

	# 파일 읽기
	with fo.open('Sample.txt', 'r') as f:
		print(f.read())
		f.close()
```
