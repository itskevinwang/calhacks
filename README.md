# calhacks

Telehealth Mobile App created for CalHacks hack:now

Our application uses autoencoders, a deep learning architecture that learns to compress input data into a smaller representation (encoder) and then expands that input data back into its original information (decoder). Our app works by running the user's encoder locally on their video (lowering required upload speed) before transmitting as well as running the other caller's decoder (lowering required download speed).

On the user's first time using the app and each time they change environments, they are asked to record a 30 second video of themselves talking. We have the user upload this video to our servers, where we use this data to fine-tune their own personal model to work for their environment the most efficiently as possible. Models are then pruned and quantized to run more efficiently. The model is split into encoder and decoder and stored under their UID in Google Cloud.

Files:

converted_model.tflite - Not the final model, but an easy model to test with.
