Clean up S3
aws s3 rm --recursive s3://omada-datascience-development/wlr

Sync using an S3 location
aws s3 sync \
    natural_language_processing/ \
    s3://omada-datascience-production/evan/natural_language_processing

other side
aws s3 sync \
    s3://omada-datascience-production/evan/natural_language_processing \
    natural_language_processing/



Watch gpu usage
watch -n 0.5 nvidia-smi
or
pip install gpustat
watch -n 0.5 -c gpustat -cp --color

Watch cpu usage
htop
(yum install htop)


python3 -m pip install -r logos/requirements.min.txt
export PYTHONPATH=$PYTHONPATH:/home/ec2-user/SageMaker/natural_language_processing/
