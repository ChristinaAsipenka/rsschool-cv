# Christina Asipenka
## PHP Developer
***
## Contacts
**E_MAIL:** [krystinabutko@gmail.com](mailto:krystinabutko@gmail.com)

**Phone:** +48 452 202 441

**Location:** Poland

**Linkedin** [Christina Asipenka](https://www.linkedin.com/in/christina-asipenka-b19a6513b)

**Full CV** [CV Link](https://github.com/ChristinaAsipenka/rsschool-cv/blob/gh-pages/CV/Christina_Asipenka_PHP_Developer.pdf)

## Profile

PHP developer with 4+ years of experience in web development. Have a solid
knowledge of Symfony and Laravel frameworks, JavaScript, SQL.
I’m focused on writing clean and maintainable code using design patterns, good
architecture and SOLID principles. I always apply a creative approach to offer
the best solutions for every project to customers. I am a perfect team player,
detail oriented and hard-working developer. Ready to master new technologies
and approaches.
***
## Skills

* PHP (Symfony, Laravel, CMS)
* Docker
* PHPUnit
* Design Patterns
* JS (Vue.js)
* SQL (MySQL, MariaDB)
* RabbitMQ
* Linux (Ubuntu)
* Git (GitLab, Bitbucket)
* CI/CD
* Jira
* SCRAM
* HTML, CSS
****

## Code example

```php
<?php
declare(strict_types=1);

namespace App\Service;

use App\Entity\MoneyEntity;
use App\Entity\TransactionEntity;
use App\Interface\CalculatorInterface;
use Symfony\Component\String\Exception\RuntimeException;

class CalculateCommissionService
{
    private array $calculatorMap;

    public function __construct(private readonly iterable $calculators)
    {
        foreach ($this->calculators as $calculator) {
            $this->calculatorMap[$calculator->getType()] = $calculator;
        }
    }

    public function calculate(TransactionEntity $data): MoneyEntity
    {
        return $this->getCalculator($data->getOperationType())->calculate($data);
    }

    private function getCalculator(string $operationType): CalculatorInterface
    {
        try {
            return $this->calculatorMap[$operationType];
        } catch (\Throwable $e) {
            throw new RuntimeException(sprintf('There is not any calculator for provided operation: %s', $this->calculatorMap[$operationType]));
        }
    }
}
```
***
## Education

**Belorussian State College of Telecommunications**

_Telecommunications Network Technician (Software)_
***
## Work Experience

* _PHP developer_ **AndersenLab** 10/2022 - 03/2024
* _Lead Software Developer_ **Belorussian State Energy and Gas Supervision** 10/2017 - 09/2022
* _Full-stack developer_ **E-Commerce websites** 01/2017 - 10/2017
* _Software Developer_ **Open Joint Stock Company “Vitebsk Factory of Electrical Tools”** 08/2006 - 09/2016
***
## Languages
* Russian - _native_
* English - _B2_
* Polish - _A2_
