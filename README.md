# Magento 2 Module: CronSemaphore

## How to use

Use it when you create a custom field that will contains a cron expression:

    <field id="cron_expression" translate="Cronexpression"
                       type="text" sortOrder="100" showInDefault="1" showInWebsite="0" showInStore="0">
                    <label>Cron Tab String</label>
                    <comment><![CDATA[
    <pre>
    * * * * *
    | | | | |
    | | | | +---- Day of the Week   (range: 0-6, 1 standing for Monday)
    | | | +------ Month of the Year (range: 1-12)
    | | +-------- Day of the Month  (range: 1-31)
    | +---------- Hour              (range: 0-23)
    +------------ Minute            (range: 0-59)
    Example: 0 0 * * * Daily at midnight
    </pre>
                    ]]></comment>
                    <validate>required-entry cronexpression</validate>
                </field>
