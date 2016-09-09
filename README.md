# projetos2
//trabalho segundo semestre, turma 2015, professor: aldebaro
controle = 0 %variavel de controle
while controle == 0
    clear all
    clc
    webcamlist %Lista os dispositivos WEBCAM instalados 
    cam = webcam; % A variavel "cam" recebe os dados da webcam 
    img = snapshot(cam); % Adquirir uma única imagem da câmera
    faceDetector = vision.CascadeObjectDetector;
    bboxes = step(faceDetector, img);
    imshow(img), title('Detected faces');hold on
    for i=1:size(bboxes,1)
        rectangle('Position',bboxes(i,:),'LineWidth',2,'EdgeColor','y');
    end
 controle = 0
end
//ilana
