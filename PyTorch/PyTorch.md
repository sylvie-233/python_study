# PyTorch

>Author: Sylvie233
>
>Date: 2022/11/29
>
>Porint: 


## 基础介绍




## 核心内容

```
torch:
	nn:
		functional:
			log_softmax():
			nll_loss():
			relu():
		Conv2d:	
			in_channels:
			out_channels:
			kernel_size:
		CrossEntropyLoss:
			
		Flatten:
		Linear:
		Module:
		ReLU:
			inplace:
	optim:
		Adam:
			step():
		SGD:
			params:
			lr:
	utils:
		data:
			DataLoader:
				__iter__():
				dataset:
				batch_size:
				shuffle:
			Dataset:
				__getitem__():
				__len__():
	Size:
	Tensor:
		
	argmax():
	load():
	save(): 模型保存
	

torchvision:
	datasets:
		mnist:
			MNIST:
				root:
				train:
				transform:
				download:
		voc:
			VOCDetection:
			VOCSegmentation:
		ImageFolder:
			root:
			transform:
			target_transform:
	models:
		vgg16:
			load_state_dict():
	transforms:
		Compose:
		Normalize:
			mean:
			std:
		RandomHorizontalFlip:
		RandomResizedCrop:
			size:
		ToTensor:

sklearn:
	datasets:
		load_iris(): 
	model_selection:
		train_test_split:

numpy:
	array():
	


pandas:



matplotlib:
	pyplot:
		plt:
			imshow():
```