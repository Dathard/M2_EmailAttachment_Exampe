Example using created preference (`\Dathard\EmailAttachment\Model\Mail\Template\TransportBuilder::addAttachment`)


````php
class SenderBuilder extends \Magento\Sales\Model\Order\Email\SenderBuilder
{
    protected function configureEmailTemplate()
    {
        parent::configureEmailTemplate();

        $attachmentFilePath = 'test.txt';

        $this->transportBuilder->addAttachment(
            file_get_contents($taxExemptCertPath),
            'example.txt',
            mime_content_type('test.txt')
        );
    }
}
````
