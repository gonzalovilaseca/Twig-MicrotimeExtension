<?php
/**
 * Twig extension for displaying microtimes in a human readable way
 *
 * @author Gonzalo Vilaseca
 * @date 04/04/2014
 */

namespace Foo\Bar;


/**
 * Class MicrotimeExtension
 * @package Sylius\Bundle\JobSchedulerBundle\Twig
 */
class MicrotimeExtension extends \Twig_Extension{

    /**
     *
     * @return array
     */
    public function getFilters()
    {
        return array(
            new \Twig_SimpleFilter('microtime_date', array($this, 'microtimeDateFilter')),
            new \Twig_SimpleFilter('microtime_exec_time', array($this, 'microtimeExecTimeFilter')),
        );
    }

    /**
     * Returns microtime in a human readable format
     *
     * @param $microtime
     *
     * @return null|string
     */
    public function microtimeDateFilter($microtime)
    {
        if (is_null($microtime)){
            return null;
        }

        $date = date("Y-m-d H:i:s",$microtime);

        return "$date";
    }

    /**
     * Returns duration
     *
     * @param $microtimeStart
     * @param $microtimeEnd
     *
     * @return string
     */
    public function microtimeExecTimeFilter($microtimeStart, $microtimeEnd)
    {
       if (is_null($microtimeStart) || is_null($microtimeEnd)){
            return '0:0';
       }

       $duration = date('i:s', $microtimeEnd - $microtimeStart);

       return "$duration";
    }

    /**
     *
     * @return string
     */
    public function getName()
    {
        return 'microtime_extension';
    }
} 
